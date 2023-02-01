### Utilities

Reduce image upload size

```ts
import uniqid from "uniqid";

export async function resizeImage(file: File) {
  const reduce = require("image-blob-reduce")();
  const blob = new Blob([file], { type: "image/jpeg" });
  const resizedBlob = await reduce.toBlob(blob, { max: 1024 });
  const resizedFile = new File([resizedBlob], `${uniqid()}.jpeg`);

  return resizedFile;
}
```

Example

```ts
  const handleUpload = async () => {
    if (files.length < 5) {
      toast({
        title: "You need to upload at least 5 photos",
        duration: 3000,
        isClosable: true,
        position: "top-right",
        status: "error",
      });
      return;
    }

    const filesToUpload = Array.from(files);
    setUploadState("uploading");

    for (let index = 0; index < filesToUpload.length; index++) {
      const file = await resizeImage(filesToUpload[index]);
      const { url } = await uploadToS3(file);

      setUrls((current) => [...current, url]);
    }

    setUploadState("uploaded");
  };
  ```

## Git Commands

Clone the repo

```bash
git clone <repo>
```

When you want to start a new feature, create a new branch

```bash
git branch <new-branch>
```

Check to see if the new branch was created

```bash
git branch
```

To switch to the new branch

```bash
git checkout <branch-name>
```

Alternatively the git checkout command accepts a -b argument that will create the new branch and immediately switch

```bash
git checkout -b <branch-name>
```

### Making a pull request

Commit the branch with a descriptive message

```bash
git commit -a -m "Added a cool new feature"
```

Push to the branch

```bash
git push origin <branch-name>
```

## Docker

Install Docker Desktop

```bash
docker --version
```

## Bash

### Bash Scripting

Change directory, make a new directory - javascript, and list the contents of the current directory

```bash
cd /path/
mkdir javascript
ls
  javascript
```

Delete a directory

```bash
rm -r directory-name
```

Project working directory
  
  ```bash
  pwd
  ```

Copy a file to directory
  
  ```bash
  cp main.js javascript 
  ```

### Powershell

Rename a directory

```
Rename-Item "directory"
```

Supply values for the following parameters:
NewName:

```
new-directory
```

## Prisma

Install the dependancies

```bash
npm i --save-dev prisma typescript ts-node @types/node nodemon
```

Create tsconfig.json

```json
{
  "compilerOptions": {
    "sourceMap": true,
    "outDir": "dist",
    "strict": true,
    "lib":["esnext"],
    "esModuleInterop": true,
  }
}
```

```bash
start a new prisma project with postgresql
```

 ```bash
  npx prisma init --datasource-provider postgresql
  ```

  Initialize the prisma client will create the following

  prisma/schema.prisma
  .env
  .gitignore

Update the schema.prisma file to include models and run the command. The command will create prisma/migrations/timesatmp/migrations.sql

```bash
npx prisma migrate dev --name init
```

Install the Prisma Client

```bash
npm i @prisma/client
```

To manually generate the client run

```bash
npx prisma generate
```

### Prisma commands

  ```bash
  npx prisma format
  ```

To log all of your prisma queries

```ts
const prisma = new PrismaClient({ log: ["query"] });
```

### Vercel

To link environment variables

```bash
vercel link
```

```bash
vercel env pull env.local
```

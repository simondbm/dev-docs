# Component Libraries

## Table of Contents

### Linting Errors

#### Cheat Sheets

<a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">Cheat Sheet</a>

To create inline HTML in markdown, use the following syntax:

#### MD033 - Inline HTML

MD033 no-inline-html HTML. Add the html tag to the allowed_elements array in the .markdownlint.json file.

```json
{
  "MD033": {
    "allowed_elements": ["a"]
  }
}
```

<span>Click <a href="https://github.com/DavidAnson/markdownlint/blob/main/doc/md033.md" target="_blank">here</a> for more information
</span>

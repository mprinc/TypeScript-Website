---
display: "Files"
oneline: "Include a list of files. This does not support glob patterns, as opposed to `include`."
---

Specifies an <span class='definition'>allowlist of files to include in the program</span>. An error occurs if any of the files <span class='important'>can't be found</span>.

```json tsconfig
{
  "compilerOptions": {},
  "files": [
    "core.ts",
    "sys.ts",
    "types.ts",
    "scanner.ts",
    "parser.ts",
    "utilities.ts",
    "binder.ts",
    "checker.ts",
    "tsc.ts"
  ]
}
```

This is useful when you only have a small number of files and <span class='important'>don't need to use a glob</span> to reference many files.
If you need that then use [`include`](#include).

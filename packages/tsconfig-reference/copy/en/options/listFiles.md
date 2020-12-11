---
display: "List Files"
oneline: "Print all of the files read during the compilation."
---

<span class='definition'>Print names of files part of the compilation</span>. This is useful when you are <span class='definition'>not sure that TypeScript has
included a file you expected</span>.

For example:

```
example
├── index.ts
├── package.json
└── tsconfig.json
```

With:

```json tsconfig
{
  "compilerOptions": {
    "listFiles": true
  }
}
```

Would echo paths like:

```
$ npm run tsc
path/to/example/node_modules/typescript/lib/lib.d.ts
path/to/example/node_modules/typescript/lib/lib.es5.d.ts
path/to/example/node_modules/typescript/lib/lib.dom.d.ts
path/to/example/node_modules/typescript/lib/lib.webworker.importscripts.d.ts
path/to/example/node_modules/typescript/lib/lib.scripthost.d.ts
path/to/example/index.ts
```

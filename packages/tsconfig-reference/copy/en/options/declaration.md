---
display: "Declaration"
oneline: "Emit d.ts files for referenced files in the project"
---

<span class='definition'>Generate `.d.ts` files for every TypeScript or JavaScript file inside your project</span>.
These `.d.ts` files are <span class='definition'>type definition files</span> which describe the <span class='important'>external API of your module</span>.
With `.d.ts` files, tools like TypeScript can provide intellisense and accurate types for un-typed code.

When `declaration` is set to `true`, running the compiler with this TypeScript code:

```ts twoslash
export let helloWorld = "hi";
```

Will generate an `index.js` file like this:

```ts twoslash
// @showEmit
export let helloWorld = "hi";
```

With a corresponding `helloWorld.d.ts`:

```ts twoslash
// @showEmittedFile: index.d.ts
// @showEmit
// @declaration
export let helloWorld = "hi";
```

<span class='important'>When working with `.d.ts` files for JavaScript</span> files you may want to use [`emitDeclarationOnly`](#emitDeclarationOnly) or use [`outDir`](#outDir) to ensure that the JavaScript files are not overwritten.

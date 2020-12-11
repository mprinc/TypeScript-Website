---
display: "Base Url"
oneline: "Set a baseurl for relative module names"
---

Lets you set a base directory to resolve non-absolute module names.

You can define a root folder where you can do <span class='definition'>absolute file resolution</span>. E.g.

```
baseUrl
├── ex.ts
├── hello
│   └── world.ts
└── tsconfig.json
```

With `"baseUrl": "./"` inside this project TypeScript will look for files starting at the same folder as the `tsconfig.json`.

```ts
import { helloWorld } from "hello/world";

console.log(helloWorld);
```

<span class='definition'>If you get tired of imports always looking like `"../"` or `"./"`</span>. Or <span class='important'>needing
to change as you move files</span>, this is a great way to fix that.

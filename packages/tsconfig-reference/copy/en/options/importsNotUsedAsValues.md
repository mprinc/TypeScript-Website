---
display: "Imports Not Used As Values"
oneline: "Controls which syntax you use for importing types"
---

<span class='definition'>This flag controls how `import` works</span>, there are 3 different options:

- `remove`: The default behavior of dropping `import` statements which only reference types.

- `preserve`: Preserves all `import` statements whose values or types are never used. <span class='definition'>This can cause imports/side-effects to be preserved</span>.

- `error`: This preserves all imports (the same as the preserve option), but <span class='important'>will error when a value import is only used as a type</span>. This might be useful if you want to ensure no values are being accidentally imported, but still make side-effect imports explicit.

This flag works because you can use `import type` to explicitly create an `import` statement which should never be emitted into JavaScript.

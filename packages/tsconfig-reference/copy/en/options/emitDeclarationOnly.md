---
display: "Emit Declaration Only"
oneline: "Only output d.ts files and not JavaScript files."
---

_Only_ emit `.d.ts` files; <span class='definition'>do not emit `.js` files</span>.

This setting is useful in two cases:

- You are using a transpiler other than TypeScript to generate your JavaScript.
- You are using TypeScript to only generate `d.ts` files for your consumers.

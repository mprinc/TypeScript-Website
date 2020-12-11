---
display: "Disable Source Project Reference Redirect"
oneline: "Use d.ts files as the source of truth for tooling between composite project boundries"
---

When working with [composite TypeScript projects](/docs/handbook/project-references.html), this option provides a way to go [back to the pre-3.7](/docs/handbook/release-notes/typescript-3-7.html#build-free-editing-with-project-references) behavior where <span class='definition'>d.ts files were used to as the boundaries between modules</span>.
In 3.7 <span class='definition'>the source of truth is now your TypeScript files</span>.

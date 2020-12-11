---
display: "Assume Changes Only Affect Direct Dependencies"
oneline: "A drastically faster, but occasionally inaccurate watch mode option."
---

When this option is enabled, TypeScript will avoid rechecking/rebuilding all <span class='important'>truly possibly-affected files</span>, and <span class='definition'>only recheck/rebuild files that have changed as well as files that directly import them</span>.

This can be considered a 'fast & loose' implementation of the watching algorithm, which can <span class='definition'>drastically reduce incremental rebuild times</span> at the expense of having to <span class='important'>run the full build occasionally to get all compiler error messages</span>.

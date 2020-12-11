---
display: "Exclude"
oneline: "Files or patterns to be skipped from the include option"
---

Specifies an array of filenames or patterns that should be <span class='definition'>skipped when resolving `include`</span>.

<span class='important'>**Important**: `exclude` _only_ changes which files are included as a result of the `include` setting</span>.
<span class='important'>A file specified by `exclude` can still become part of your codebase</span> <span class='definition'>due to an `import` statement</span> in your code, a `types` inclusion, a `/// <reference` directive, or being specified in the `files` list.

It is <span class='definition'>not a mechanism that **prevents**</span> a file from being included in the codebase - it simply <span class='definition'>changes what the `include` setting finds</span>.

---
display: "disableReferencedProjectLoad"
oneline: "Reduce the number of projects loaded automatically by TypeScript."
---

In <span class='definition'>multi-project TypeScript programs</span>, TypeScript will load all of the available projects into memory in order to provide accurate results for editor responses which require a full knowledge graph like <span class='definition'>'Find All References'</span>.

If your project is large, you can use the flag `disableReferencedProjectLoad` to disable the automatic loading of all projects. Instead, <span class='important'>projects are loaded dynamically</span> as you open files through your editor.

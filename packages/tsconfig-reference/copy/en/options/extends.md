---
display: "Extends"
oneline: "Inherit options for a TSConfig"
---

The value of `extends` is a string which contains a <span class='definition'>path to another configuration file</span> to inherit from.
The path may use Node.js style resolution.

<span class='important'>The configuration from the base file are loaded first</span>, then <span class='important'>overridden</span> by those in the inheriting config file. All relative paths found in the configuration file will be <span class='important'>resolved</span> relative to the configuration file they originated in.

<span class='important'>It's worth noting that `files`, `include` and `exclude` from the inheriting config file _overwrite_ those from the
base config file</span>, and that circularity between configuration files is not allowed.

Currently, the only top-level property that is excluded from inheritance is [`references`](#references).

##### Example

`configs/base.json`:

```json tsconfig
{
  "compilerOptions": {
    "noImplicitAny": true,
    "strictNullChecks": true
  }
}
```

`tsconfig.json`:

```json tsconfig
{
  "extends": "./configs/base",
  "files": ["main.ts", "supplemental.ts"]
}
```

`tsconfig.nostrictnull.json`:

```json tsconfig
{
  "extends": "./tsconfig",
  "compilerOptions": {
    "strictNullChecks": false
  }
}
```

Properties with relative paths found in the configuration file, which aren't excluded from inheritance, will be resolved relative to the configuration file they originated in.

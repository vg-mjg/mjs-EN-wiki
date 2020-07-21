# Advanced concepts

## Tools

### Mod types

Resource packs, JS extensions, tool
（请注意区分**拓展**和**扩展**，如果有想到什么名字概括这三个也可以 issue 提醒）

### Description

It uses JSOn language to describe the mod
### Metadata

Shown below：

```typescript
export interface Metadata {
  id: string
  version: string
  name?: string
  author?: string | string[]
  description?: string
  preview?: string
  dependencies?: { [key: string]: string }
}
```

Only ID and version are mandatory. Full list here:

| Field         | Format restriction            | Description                                                               |
| ------------ | ------------------- | ------------------------------------------------------------------ |
| id           | `/^[_a-zA-Z0-9]+$/` | mod name，**must be the same as folder name**                   |
| version      | `semver`            | version of the mod (tl;dr x.x.x numbers) https://semver.org/ |
| name         | 无                  | mod name in mjs                                                             |
| author       | 无                  | author name，with `string[]` you can cite more                               |
| description  | 无                  | description                                                         |
| preview      | 无                  | Preview image, default is `preview.png` **（note：`1.x` for `jpg`）**          |
| dependencies | 见下                | prevent it to run if it doesn't have the dependencies                                     |

### JSON 

### Dependency

MJS+ checks for dependencies before running
### Load order

MJS+ loads in order of selection, if there are conflicts, the latter overwrites the former.
### Check order

Brief check order explanation：

1. Check if ID is consistent with `/^[_a-zA-Z0-9]+$/`
1. Check if folder=ID
1. Check if ID is unique
1. Check JSON Schema
1. Check version

If one doesn't pass, the mod isn't shown in MJS+

### Note

Don't manually change `active.json`.

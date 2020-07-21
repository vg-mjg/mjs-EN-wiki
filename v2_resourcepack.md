# Resource Pack

For an overview, read this article. For more details, check [here](v2_resourcepack_advanced).

Resource packs replace files in the `static/v0.5.1.w` folders with user-chosen ones.

## Format

Resource pack format is shown below：

```
- resource_pack_name
  - resourcepack.json
  - assets
    - folderA
      - fileBinFolderA.png
    - fileA.png
```

resource_pack.json describes the mod, while `assets` folder contains the new files.

## resource_pack.json

Here is a sample of a `resource_pack.json`：

```jsonc
{
  // metadata
  "id": "sample", // folder name
  "version": "1.0.0", // version
  "name": "sample_pack", // mod name
  "author": "Majsoul Plus Team", // author
  "description": "This is a sample resource pack.", // description
  "preview": "preview.png", // preview image

  // dependency, if needed
  "dependencies": {
    "majsoul_plus": "^2.0.0" // form 2.0.0 and up
  },
  "replace": [
    "audio/sound/zeniya/fan_dora10.mp3",
    "scene/Assets/Resource/mjpai/en/mjp_default_0/8p.png",
    {
      "from": [
        "audio/sound/qianzhi/lobby_normal1.mp3",
        "audio/sound/qianzhi/lobby_normal2.mp3",
        "audio/sound/qianzhi/lobby_normal3.mp3",
        "audio/sound/qianzhi/lobby_normal4.mp3",
        "audio/sound/qianzhi/lobby_normal5.mp3"
      ],
      "to": "audio/quack.mp3"
    }
  ]
}
```

## What about scripts？

Resourcepacks can't run javascript. That functionality is implemented in [extensions](v2_extension)。

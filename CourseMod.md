# Mods

This page will teach you about mods for [MJS+](https://github.com/MajsoulPlus/majsoul-plus)』

## Before

- text editor
- [JSON knowledge](https://github.com/MajsoulPlus/majsoul-plus/wiki/JsonFormat)

## File structure

- Data cache folder
  - `Majsoul Plus/static/`

> **Warning** Don't change contents directly in /static

- Extensions
  - `Majsoul Plus/extension`
- Resource Packs
  - `Majsoul Plus/resourcepack`
- Tools
  - `Majsoul Plus/tool`

> **Note：**  Folder will be in `%appdata%/Majsoul Plus` for Windows users, while in `.config/Majsoul Plus` for Linux users.

## Create a new mod

1. In the correct location, create a  `mymod` folder；

2. In the mod folder, create a `extension.json` or `resourcepack.json` ：

```json
{
{
  "id": "washizu",          folder name
  "version": "2.0.0",       version number
  "name": "Washizu",        mod name
  "author": ["anons"],      author name
  "description": "Replace hags with emperors. If you can find the missing yaku, say in thread.",        description
  "preview": "preview.png", preview image
  "resourcepack": [
    "extendRes/charactor/erjietang/bighead.png",  file 1 to replace
    "extendRes/charactor/erjietang/full.png"      file 2 to replace
  ],
  "entry": "script.js"      script to run
}
}
```

3. Default media folder is `assets`

4. Only id and name are mandatory fields

## Tl;dr repo guide

1. To replace `static/0/v0.4.1.w/scene/Assets/Resource/tablecloth/tablecloth_default/Table_Dif.jpg`: you need to place the new file in `assets (in the mod folder)/scene/Assets/Resource/tablecloth/tablecloth_default`, and add it into the `.json`

2. To run `script.js`: place it in the mod folder, then add `"entry": "script.js"` to the `.json`

## Test

Open MJS+, your mod should be there in the right tab if you worked correctly. Switch it on and start the game.
If you encounter no problems, press `Edit` button, then the package one to export it into a `.mspe``.msrp`
## JS help
[Javascript guide](https://javascript.info/)

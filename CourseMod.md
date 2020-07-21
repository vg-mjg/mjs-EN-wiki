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
  "id": "washizu", //folder name
  "version": "2.0.0", //version number
  "name": "Washizu", //mod name
  "author": ["anons"], //author name
  "description": "Replace hags with emperors. If you can find the missing yaku, say in thread.", //description
  "preview": "preview.png", //preview image
  "resourcepack": [
    "extendRes/charactor/erjietang/bighead.png",  //tiles to replace
    "extendRes/charactor/erjietang/full.png"
  ],
  "entry": "script.js"   //script to run
}
}
```

3. 在模组文件夹中，根据 `mod.json` 文件中 `dir` 的值创建文件夹，默认值为 `/files`；

4. （可选）推荐在模组文件夹中，创建一张矩形图像并指定给 `mod.json` 的 `preview` 属性作为预览图。

## 简易制作模组流程

1. 从「游戏数据缓存目录」中找到想要修改的内容，保持相同的相对路径，复制文件到模组文件夹中；

如：要替换的文件为 `/resources/app/static/0/v0.4.1.w/scene/Assets/Resource/tablecloth/tablecloth_default/Table_Dif.jpg`

你需要建立路径：

`/resources/app/mod/mymod/files/0/v0.4.1.w/scene/Assets/Resource/tablecloth/tablecloth_default`

> 缓存目录有时不会包含您希望替换的资源，您可以尝试启动游戏并确保要替换的资源已经被加载后再次尝试。

2. 修改 `mod.json` 文件中的 `"name"` 条目为「模组的名称」；

3. 修改 `mod.json` 文件中的 `"author"` 条目为「作者的名字」；

4. 修改 `mod.json` 文件中的 `"description"` 条目为「模组的简介」；

5. 对已经复制的内容进行编辑或替换。

## 测试&打包模组

打开雀魂 Plus 浏览器，选择左侧的「模组」标签页，若步骤进行无误，您应该已经可以在右侧面板中找到您的模组。模组右下角的开关默认为未启用状态，在您启用后，就可以启动游戏进行测试了。

测试无问题后，点击右上角纸笔图案的「编辑」按钮，此时模组右下角的开关位置变为了删除和打包选项（再点击一次「编辑」按钮可恢复），点击打包并选择保存位置即可。

## 附录：进阶功能

清单文件中的 `replace` 字段与 `execute` 字段均为可选功能：

- 前者可将不同路径的文件指向同一替换文件，一定程度上防止版本更新造成的模组失效 & 避免重复文件难以维护，需要一定正则表达式基础
- 后者可运行自定义脚本以完成一些高级功能，需要一定 `Javascript` 基础（具体请参考 `README` 文档中[开发插件](https://github.com/MajsoulPlus/majsoul-plus#开发插件)部分）

[正则表达式入门教程](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions)

[Javascript 入门教程](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps)

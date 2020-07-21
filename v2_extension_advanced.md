# Extension（Advanced）

## Local file

To get `test/assets/1.txt`，write：

```js
fetch(`${document.location.href}majsoul_plus/extension/test/1.txt`).then(
  ctx => {
    // code.png
  }
)
```

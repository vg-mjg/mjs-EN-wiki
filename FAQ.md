# FAQ

## Why did a mod installation fail？

1. Check the file extension is one of `*.mspm`,`*.mspe`,`*.mspt`
2. Check there are only english characters in the name
3. Check that name isn't too long

## Will I get banned using MJS+？

In principle it's no different from using any browser and there's no modification in the communication with MJS servers,
thought it is no guarantee that Yostar won't ban you. 

## Why is the cache folder xx ？

Cache is built on your requests to the server, so if you don't need some resource it won't build up.

## Why doesn't MJS+ save the login informations？
MJS+ will automatically build a proxy server to facilitate the loading of the local cache. By default the 8887 port is used as the proxy server port. If it's occupied it will use another port, but you will lose automatic login.
If login info aren't saved, prevent other softwares from using 8887 port.

## Black screen？

1. Confirm your internet connection；
2. If you can play from other browsers, report an [issue](https://github.com/MajsoulPlus/majsoul-plus-client/issues/new/choose)

## Why does MJS+ uses so much CPU and memory？

1. MJS uses Laya engine, that produces a big system load；
2. Plugins will occupy some RAM and CPU resources；
3. Electron kernel dynamically requests many resources to ensure a working speed. (??)

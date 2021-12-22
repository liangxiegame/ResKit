# ResKit

一套资源管理工具

由 QFramework 团队官方维护的独立工具包（不依赖 QFramework）。

## 环境要求

* Unity 2018.4LTS

## 安装

* PackageManager
    * add from package git url：https://github.com/liangxiegame/ResKit.git 
    * 或者国内镜像仓库：https://gitee.com/liangxiegame/ResKit.git
* 或者[点此下载 ResKit.unitypackage](ResKit.unitypackage) 并安装到自己项目中的任意脚本中

## 使用指南

``` csharp
// allocate a loader when initialize a panel or a monobehavour
var loader = ResLoader.Allocate();

// load someth in a panel or a monobehaviour
loader.LoadSync<GameObject>("resources://smobj");

loader.LoadSync<Texture2D>("resources://Bg");

// load by asset bundle's assetName
loader.LoadSync<Texture2D>("HomeBg");

// load by asset bundle name and assetName
loader.LoadSync<Texture2D>("home","HomeBg");


// resycle this panel/monobehaivour's loaded res when destroyed 
loader.Recycle2Cache();
loader = null;
```



## 更多

* QFramework 地址: https://github.com/liangxiegame/qframework


# Smart Autodetection
# SDK 智能检测

Available Functions(这玩意用来干啥)
--------------------

This is a new version for [Smart Autodetection](https://github.com/aayvazyan-tgm/autodetect_android_sdk_and_buildTools/).The origin code is too old to run on modern Android SDK, Then I fix by by a little work.

这是 [Smart Autodetection](https://github.com/aayvazyan-tgm/autodetect_android_sdk_and_buildTools/) 的一个新版本。原先的代码是道光年间写的现在跑不动了，所以我做了一点微小的工作让它可以至少跑起来。

The code is dirty but at least it works : ）

我用来修复的代码挺艹蛋的不过至少好使。

Usage(这玩意咋用)
------------

See [the origin document](https://github.com/aayvazyan-tgm/autodetect_android_sdk_and_buildTools)

哥们，我相信你的水平点[上面的链接](https://github.com/aayvazyan-tgm/autodetect_android_sdk_and_buildTools)你是能看懂的。

算了，还是写上吧。

```gradle
apply from: 'https://raw.githubusercontent.com/undownding/autodetect_android_sdk_and_buildTools/master/sdktools.gradle'

android {
    //use the newest SDK automatically if the given one is not available
    compileSdkVersion project.getSDKIfPossible(21)
    //Use the lastest patch BuildTool Version available, that fits to the given minor version. default to the given value on error
    buildToolsVersion project.getHighestAvailableTools("21.1.2")
}
```

Not work in China.See offline usage.

因为众所周知的原因上面这写法八成是不好使的，还是老老实实把脚本扒下来本地引用吧。

```gradle
apply from: 'sdktools.gradle'
```

Attention(注意)
------------
cmd.exe not work on my computer so I use PowerShell, if you're using windows, please at lease confirm PowerShell.exe works.

Windows 环境下至少我的电脑上用 cmd 调用是不好使的，所以我直接用 PowerShell 了。我不知道 Windows 7 下好使不，至少我的 Windows 10 是有的。要是你用的 Windows 7 发现这脚本不好使了，你还是自己调好了。




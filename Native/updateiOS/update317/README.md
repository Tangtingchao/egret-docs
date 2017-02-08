## 更新内容

* [修复] 修复设置非法颜色值造成游戏崩溃的问题；
* [修复] 解决首次启动游戏一定会进行热更新的问题；
* [修复] 修复字体描边颜色显示异常的问题；
* [修复] 补全声音播放事件；
* [修复] 修复不能在播放过程中修改音量的问题；
* [新特性] 支持斜体文本；
* [新特性] 添加ColorTransform滤镜；
* [改进] 比对热更新文件时不再显示进度条；
* [改进] 热更新地址不存在时启动最后一次更新的游戏包；
* [改进] 提高稳定性。

	将下面这的语句放在rungame函数下可以解决首次启动一定会进行热更新的问题：

	~~~
//设置忽略的热更新版本地址，如果监测到当前热更新游戏包和设置的一样，就直接启动本地的游戏包。用于避免首次启动游戏一定会进行热更新的问题。
[EgretRuntime getInstance] setIgnoreVersion:(@"http://127.0.0.1/test/egret-game_XXX.zip")];
~~~
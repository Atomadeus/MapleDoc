# 冒险岛开源实现

冒险岛开源实现，支持Windows,macOs,Android,iOS

## 设计文档
（陆续更新中......）

* [窗口以及坐标系](./client/engine/窗口以及坐标系.md)
* [主循环的设计](./client/engine/主循环设计.md)
* [事件系统的设计与实现](./client/engine/事件系统的设计与实现.md)
* [纹理管理](./client/engine/纹理管理.md)
* [字体管理](./client/engine/字体管理.md)
* [时钟管理](./client/engine/时钟管理.md)
* [音频实现](./client/audio/跨平台Audio实现.md)
* [网络:网络层架构](./client/network/网络层的实现.md)
* [网络:断线重连](./client/network/reconnect.md)
* [安全:防修改](./client/gameplay/防作弊.md)
* [安全:安卓客户端加固策略]
* [MapleStory 客户端参数解析]
* [MapleStory 物理引擎]
* [MapleStory 场景管理策略]
* [跨平台持久化]
* [脚本:客户端lua support]
* [脚本:客户端:NPC:本地lua交互]
* [脚本:服务端:Java/JavaScript]
* [UI:UI层架构设计]
* [UI:UI组件设计]
* [UI:TextView]
* [UI:EditText]
* [UI:Button]
* [UI:ProgressBar]

## Getting Started

目前进度80%，暂无开源打算

### 依赖库

[glfw3](https://github.com/glfw/glfw) [glew](https://github.com/nigels-com/glew) [glfm](https://github.com/brackeen/glfm) [bass](http://www.un4seen.com/) pvmp3 [asio](http://think-async.com/Asio) [freetype2](https://www.freetype.org/) [iconv](http://www.gnu.org/software/libiconv/) [lua](http://www.lua.org/) [openal](www.openal.org/
) [sqlite](https://www.sqlite.org/) [xxhash](https://github.com/Cyan4973/xxHash) [zlib](www.zlib.net/
) 

Thanks to [NoLifeStory](https://github.com/NoLifeDev/NoLifeStory)  
 [MapleLib](https://github.com/haha01haha01/MapleLib)
 [Odinms]
 

### 编译脚本

### Windows
* Visual Studio 2017
* CMake 3.10.2 or higher
* `gen_build_win_x86.bat` generate project in `build`
* `gen_build_win_x64.bat` generate project in `build`

### iOS
* Xcode
* CMake 3.10.2 or higher
* `build_ios.sh` generate project in `build`

### macOS
* Xcode
* CMake 3.10.2 or higher
* `build_mac.sh` generate project in `build`

### Android
* Android Studio
* CMake 3.10.2 or higher
* `app/project/android`

## 引擎功能

语言：
```
c++ 14 
opengl / opengles
kotlin objective-c
```

平台支持
```
OpenGL OpenGLES 2.0
Android iOS macOS Windows
```

核心功能
```
multi-platform
memory management 
memory protected（can anit cheatengine）
function callback in main-thread
event dispathcer
lua-support 
scene manager
abundant ui components
maplestory physics,camera,texture,sprite,animation
maplestory filesystem
audio 
network
```

支持外设
```
Touch
Mouse
Keyboard
Joystick
```
其他
```
UTF-8 and UTF-16 support

```

## 架构预览

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/1.png)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/audio.png)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/event.png)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/window.png)

## 截图

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/login.jpg)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/charselect.jpg)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/game.jpg)





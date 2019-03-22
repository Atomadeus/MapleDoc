# The MapleStory Open-Source Implement

The MapleStory Open-Source Implement, which support for android、ios、windows、mac、linux platform.

## Getting Started

this project has been completed 80% above . if I have completed 90% above, I would open source it .

### Prerequisites

this project is base on [glfw3](https://github.com/glfw/glfw) [glew](https://github.com/nigels-com/glew) [glfm](https://github.com/brackeen/glfm) [bass](http://www.un4seen.com/) pvmp3 [asio](http://think-async.com/Asio) [freetype2](https://www.freetype.org/) [iconv](http://www.gnu.org/software/libiconv/) [lua](http://www.lua.org/) [openal](www.openal.org/
) [sqlite](https://www.sqlite.org/) [xxhash](https://github.com/Cyan4973/xxHash) [zlib](www.zlib.net/
) 

Thanks to [NoLifeStory](https://github.com/NoLifeDev/NoLifeStory)  
 [MapleLib](https://github.com/haha01haha01/MapleLib)
 [Odinms]
 

### Build

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

## Engine Function

Program language 
```
 Using c++ 14 and opengl / opengles to implement the core framework 
 Using kotlin ,objective-c to impl specific platfrom function ,things like virbate ,touch and other event.
```

Platform support 
```
OpenGL OpenGLES 2.0
Android iOS macOS Windows
```

Engine Core Fucntion
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

Input
```
Touch
Mouse
Keyboard
Joystick
```
Others
```
UTF-8 and UTF-16 support

```

## Architecture

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/1.png)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/audio.png)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/event.png)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/window.png)

## Screenshot

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/login.jpg)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/charselect.jpg)

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/game.jpg)]





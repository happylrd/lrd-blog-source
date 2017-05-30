---
title: 初识flutter
date: 2017-05-26 19:43:36
tags:
- Flutter
- 前端
- Google
- Fuchsia
- Dart
categories:
- 技术向
thumbnail: http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/flutter-mark-square-100.png
---

> 春未老，风细柳斜斜。试上超然台上看，半壕春水一城花。烟雨暗千家。
> <div style="text-align:right"><p>——《<cite>望江南·超然台作</cite>》</p></div>

## 引子

> 随着天下公认的标准ES6的全面应用、[Web Components](https://www.webcomponents.org/)标准的如日中天，全面兼容ES6的TypeScript在与推倒重来的Dart的争锋中占尽先机，而基于Dart的Flutter又在与基于实现了Web Components标准的Angular、React、Vue而构建的Ionic（hybrid）、React Native（js-to-native）、Weex（js-to-native）的比拼中愈显势穷力屈。然而[Fuchsia](https://github.com/fuchsia-mirror)的横空出世又使得一切变得扑朔迷离...

## 简介

Flutter 是一个用来开发跨平台app的框架，构建在Dart语言之上，提供了一个 [FRP](https://en.wikipedia.org/wiki/Functional_reactive_programming) 框架，并自带了一套 *Material Design* 和 *Cupertino(iOS-flavor)* widget，从而可以使我们轻松地开发出漂亮的app。

Flutter 还对原生特性提供了很好的支持，对于 iOS or Android 开发者而言，你可以充分利用现有的 *Java、Kotlin、ObjC、Swift* 代码，并使用 Flutter 来统一app开发。

Flutter 还提供了强大的 *热重载* 机制。虽说现代web框架基本上都会提供，但 Flutter 的强大之处在于当app崩溃后可以从app停止的位置继续调试，也就是说，不会丢失app的状态。

## 环境搭建

> 仅针对Windows 用户，macOS 与 Linux 用户可移步 [Flutter Setup](https://flutter.io/setup/)。

前置条件
- Windows 7 or later (64-bit)
- [Git for Windows](https://git-scm.com/download/win)

### 安装Flutter

#### Clone仓库

`git clone https://github.com/flutter/flutter.git`

#### 配置环境变量

- GUI方式：进入`计算机->属性->高级系统设置->环境变量`，在Path环境变量最后添加`${CURRENT_DIR}\flutter\bin`。
- 命令行方式：`setx PATH "%PATH%;${CURRENT_DIR}\flutter\bin"`

`${CURRENT_DIR}`即为上一步用于clone仓库的目录。

#### 运行doctor

运行`flutter doctor`。

第一次运行会下载一些依赖，确保 **良好的网络环境** 即可。
还有就是Flutter的SDK携带了Dart的SDK，所以我们没有必要独立安装Dart。

Flutter 默认会向 google 发送报告，可以通过 `flutter config --no-analytics` 来禁止，不过还是建议大家默认就好，一起来帮助flutter成长。

至此，flutter已经安装成功。

### 开发环境配置

#### Android Studio

##### 安装 Android Studio

访问[Android Studio下载页](https://developer.android.com/studio/index.html)，下载并安装即可，安装过程非常简单，只需要确保 **良好的网络环境** 即可。

##### 配置 Android 模拟器

在`Emulated Performance`下, 选择`Hardware - GLES 2.0`来确保启用硬件加速。

![android_emulator_ha](http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/android_emulator_ha.png)

#### WebStorm

##### 安装插件

WebStorm(2017.1)已经内置了`Dart`插件，只需安装`Flutter`插件即可。

进入`File->Settings->Plugins->Browse repositories...->Flutter` 点击install，安装完成后重启IDE即可。

##### 配置Flutter插件

进入`File->Settings->Languages & Frameworks->Flutter`，
插件安装之后会自动配置`Flutter SDK path`为`${CURRENT_DIR}\flutter`，若没有，请自行更正。

![plugin_flutter_idea](http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/plugin_flutter_idea.png)

至此，开发环境搭建完成，让我们开始愉快的Flutter编程之旅吧。

## 创建第一个app

### 命令行式

执行`flutter create firstapp`创建app。

创建成功后，`cd firstapp`进入项目根目录并执行`flutter run`（执行此命令之前，确保已经启动了Android模拟器）。

### IDE式

在配置了`Flutter`插件之后，我们可以使用WebStorm来创建Flutter项目，它其实就是对`flutter cli`工具做了一层ui包装。

创建成功后，我们启动Android模拟器，

![idea_run_1](http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/idea_run_1.png)

通过IDE运行项目：

![idea_run_2](http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/idea_run_2.png)

### 执行结果

结果如下：

![flutter_first_app](http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/flutter_first_app.png)

此时访问 `http://127.0.0.1:8100/` 可以看到一个 *Observatory debugger and profiler*。

![dart_vm_observatory](http://lrd-blog-assets.oss-cn-shanghai.aliyuncs.com/image/dart_vm_observatory.png)

（完）

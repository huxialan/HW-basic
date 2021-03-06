## 介绍
此项目是一个简单的ionic App，预期包含以下几点常用功能：

1. 屏幕适配
2. 常用工具封装
3. Tab图标替换
4. 字体库替换
5. Echarts使用
6. 自定义通讯录
7. 数据库
8. 版本信息

我会抽空将其完善，供大家参考。
我的博客也放置在 `GitHub` 仓库 [Blog](https://github.com/JerryMissTom/Blog/issues) 上，里面有我在 `ionic` 实践过程中的踩坑心得，可以参考下。

## 开发环境
1. ionic V3.10.3
2. cordova V7.0.1
3. npm V5.4.1
4. node V8.1.4

## 用法

#### 初始化项目
顺序执行以下操作：
```
//空白文件夹下
git clone https://github.com/JerryMissTom/HW-basic.git

// 项目根目录下：
npm install

//安装 App Version 插件
ionic cordova plugin add cordova-plugin-app-version

//安装 Keyboard 插件
ionic cordova plugin add ionic-plugin-keyboard

//安装 Sqlite 插件
ionic cordova plugin add cordova-sqlite-storage
```
#### 打包
Android环境
确保已经安装了相应Android SDK
```
// 添加android平台
ionic cordova platform add android 

// 打包
ionic cordova build android --prod
```
然后使用 `Android Studio` 打开项目下 `platform/android` 文件夹进行签名打包


iOS 环境
确保安装Xcode，并配置好相关SDK
```
// 添加android平台
ionic cordova platform add ios 

// 打包
ionic cordova build ios --prod
```
然后使用 `Xcode` 打开项目下 `platform/ios` 文件夹进行签名打包

#### 调试
浏览器调试，适合调试界面和接口
```
ionic serve
```

安卓调试，适合调试原生功能

打开手机的开发者选项和通过USB调试，然后执行 `ionic cordova run android` 安装至手机并运行，打开Chrome浏览器，在地址栏输入 `chrome://inspect`（第一次打开需要翻墙），可以看到需要调试的APP。

# 安装

我们提供了多个平台的可执行程序，你可以点击上面的下载链接开始使用TrustNote钱包，也可以使用项目源代码编译成可执行程序。

# 依赖

1、git
2、Node.js v8.9.4
3、NW.js v0.26.6
https://dl.nwjs.io/v0.26.6
4、bower


```
npm install -g bower@1.8.2
```
grunt
```
npm install -g grunt-cli
```
nw-gyp
```
npm install -g nw-gyp
```
Windows
方法一

用管理员权限打开PowerShell，执行 npm install --global --production windows-build-tools
配置环境变量 GYP_MSVS_VERSION = 2017
npm config set msvs_version 2017
参考 windows-build-tools

方法二

安装 Visual Studio 2017，在安装选项中选择VC++ 2015 (v140)工具集。
安装 Python 2.7.14
配置环境变量 在 PATH 添加Python安装目录
配置环境变量 GYP_MSVS_VERSION = 2017
npm config set msvs_version 2017
克隆项目代码
```
git clone https://github.com/trustnote/trustnote-wallet.git
cd trustnote-wallet
```
编译项目
# ./trustnote-wallet

```
bower install
npm install
npm rebuild sqlite3 --build-from-source --runtime=node-webkit --target_arch=x64 --target=0.26.6
grunt
```

运行程序:
# ./trustnote-wallet
./nwjs/nwjs .
软件打包
在trustnote-wallet目录下操作，完成之后会在上级目录trustnotebuilds中生成安装包。

--|
  | trustnote-wallet
  | trustnotebuilds
Android
安装 Android SDK （参考 https://developer.android.google.cn/studio/）
运行 make android
iOS
安装 Xcode 9 (或最新版本)
安装 Cordova npm install -g cordova
安装 ios-deploy npm install -g ios-deploy
执行 make ios
macOS
```
make osx64
```
Windows
```
make win64
```
Linux
```
make linux64
```
TrustNote备份和恢复
TrustNote使用过程中，会在用户目录生成缓存文件，用来保存账本数据和个人设置，并且在卸载软件后不会主动删除这些缓存文件，防止错误卸载软件而丢失个人数字资产，重新安装软件就可恢复数据。若用户已确定要删除这些废弃的数据，可按照下面的操作系统位置去操作。

macOS: ~/Library/Application Support/TTT
Linux: ~/.config/TTT
Windows: %LOCALAPPDATA%\TTT
问题反馈
GitHub Issues
Email Support
许可证
MIT

# 自动部署安装IPA

原理:使用safari浏览器的解析协议 + 构建好的plist文件。在safari中输入以下字符串即可安装IPA文件(IPA需签名)。
itms-services:///?action=download-manifest&url=https://raw.githubusercontent.com/yaoliangjun/appUpgrade/master/Install/install.plist

建立Git仓库,文件结构自行参考master分支。

index.html 在ios设备上访问该页面，点击安装将会安装IPA文件,避免输入上述一大串字符串。
Install 文件夹下主要为需要安装的IPA资源包，安装过程中显示的图标，构建好的plist文件。

注意:Git默认不显示网页，需要到建好的仓库找到 Settings->GitHub Pages指定master分之为web源码发布，之后会出现一个主页地址。
Your site is published at https://yaoliangjun.github.io/appUpgrade/ 之后访问这个地址即可安装自己上传的IPA包。


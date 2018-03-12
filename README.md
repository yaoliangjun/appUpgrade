# PlistInstall
访问网址自动部署安装IPA

原理:使用safari浏览器的解析协议 + 构建好的plist文件。在safari中输入以下字符串即可安装IPA文件(IPA需签名)。
itms-services:///?action=download-manifest&url=https://raw.githubusercontent.com/LengYi/PlistInstallHD/master/Install/install.plist

建立Git仓库,文件结构自行参考master分支。

index.html 在ios设备上访问该页面，点击安装将会安装IPA文件,避免输入上述一大串字符串。
Install 文件夹下主要为需要安装的IPA资源包，安装过程中显示的图标，构建好的plist文件。

注意:Git默认不显示网页，需要到建好的仓库找到 Settings->GitHub Pages指定master分之为web源码发布，之后会出现一个主页地址。
 Your site is published at https://lengyi.github.io/PlistInstallHD/ 之后访问这个地址即可安装自己上传的IPA包。

 配置文件
 index.html 中有个plist地址，在你的文件上传GitHub之后，找到install.plist,点击改文件进入详情页,找到Raw按钮,点击Raw会打开一个网址,拷贝浏览器上面的地址即为需要的plist地址  https://raw.githubusercontent.com/LengYi/PlistInstallHD/master/Install/install.plist
 Plist文件构建中主要有两个地址一个是包地址，一个是图片地址，将其主要域名换成更plist文件一样即可。
 如果你是在Git上同样配置这些，跟我不一样的就用户名，仓库名称不一样，如果差太多的话就是错了，是不能安装成功的哦。

 其它注意事项
 		<dict>
				<key>bundle-identifier</key>
				<string>com.tongbu.tuihd.Z2H3GSNJHN</string>     // 包的sku
				<key>bundle-version</key>
				<string>3.1.1</string>				   // 包的版本号
				<key>kind</key>
				<string>software</string>
				<key>title</key>
				<string>同步推正版HD</string>          // 提示安装时弹出的名称
			</dict>

以上都改好了,再次更新Git，然后访问你的主要地址，就可以静静的等待安装了。：）。


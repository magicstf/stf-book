## Sublime Text 3 安装及常用插件配置
###Sublime Text 3 优势

1、没有学习难度，上手即用。

2、支持多点编辑。

3、基于package control强大的包管理功能。

4、闪电一样的速度。

5、深度可配置，配置方式继承了unix系统的简约透明的原则，所有的配置内容都是纯文的。

6、快速文件切换，command+p 

7、shift+command+p。

8、可启用vim模式。

9、成为业界标准。

10、社区特别活跃，遇到问题可及时得到响应。

###Sulbime Text 3 安装
官网安装地址：http://www.sublimetext.com/3（OS X,Windows,Windows 64bit,Linux 32bit,Linux 64bit）

###Sulbime Text3 插件管理器

安装插件管理器（Sublime Package Control）：https://sublime.wbond.net/installation

菜单view > Show Console 调出命令行工具粘贴命令

````
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
````

回车，重启sublime text3即可。

检查插件管理安装成功：如果Preferences > Package Control 这个选项，即表示插件管理器安装成功！

###Sulbime Text3 常用插件
1、[Emmet](https://packagecontrol.io/packages/Emmet)

功能：编码快捷键，前端必备

简介：Emmet作为zen coding的升级版，对于前端来说，可是必备插件，如果你对它还不太熟悉，可以在其官网（[http://docs.emmet.io/](http://docs.emmet.io/)）上看下具体的演示视频。

使用：教程-[http://docs.emmet.io/cheat-sheet/](http://docs.emmet.io/cheat-sheet/)

2、[sideBarEnhancements](https://packagecontrol.io/packages/SideBarEnhancements)

功能：增强侧边栏

使用：安装后重启sublime, 在项目文件上右键查看

3、[DocBlockr](https://packagecontrol.io/packages/DocBlockr)

功能：生成注释

使用：输入 /* 然后回车，还有很多用法，请参照

4、[Auto​File​Name](https://packagecontrol.io/packages/AutoFileName)

功能：自动完成文件名的输入

使用：输入”/”即可看到相对于本项目文件夹的其他文件

5、[Bracket Highlighter](https://packagecontrol.io/packages/BracketHighlighter)

功能：可匹配[], (), {}, “”, ”, <tag></tag>，高亮标记，便于查看起始和结束标记

使用：点击对应代码即可

6、[jQuery](https://packagecontrol.io/packages/jQuery)

功能：jQ函数提示

7、[Nodejs](https://packagecontrol.io/packages/Nodejs)

功能：node代码提示

教程：https://sublime.wbond.net/packages/Nodejs

8、[FileHeader](https://packagecontrol.io/packages/FileHeader)

功能：添加文件头注释

教程：http://shiyanhui.github.io/FileHeader/

9、[HTML-CSS-JS Prettify](https://packagecontrol.io/packages/HTML-CSS-JS%20Prettify)

功能：格式化html/css/js

配置：pulgin options

    "node_path":
    {
        "windows": "C:/Program Files/nodejs/node.exe",
        "linux": "/usr/bin/nodejs",
        "osx": "/Users/sutengfei/.nvm/versions/node/v6.11.5/bin/node"
    }
    
  说明：根据自己的系统，选择node的安装路径
  	
  	
10、[Browser Refresh](https://packagecontrol.io/packages/Browser%20Refresh) 

功能：保存自动刷新浏览器

配置：

	[
	  {
	    "keys": ["command+s"], "command": "browser_refresh", "args": {
	      "auto_save": true,
	      "delay": 0.0,
	      "activate": true,
	      "browsers" : ["chrome"]
	    }
	  }
	]

使用：配置好后conmand+s,即可。
说明：我用的是mac,快捷键根据自己系统自行配置

11、[Themes （主题）](https://packagecontrol.io/search/Themes)

功能：美化sublime

我的主题：[Material-Theme](https://packagecontrol.io/packages/Material%20Theme)

我的主题配置：{ "theme": "Material-Theme.sublime-theme", }

12、[A File Icon](https://packagecontrol.io/packages/A%20File%20Icon)

功能：不同文件显示不同的icon,配合主题使用

13、[Status Bar Time](https://packagecontrol.io/packages/Status%20Bar%20Time)

功能：状态栏显示当前时间

使用：安装即可显示

14、[advancedNewFile](https://packagecontrol.io/packages/AdvancedNewFile)

功能：快速创建文件

使用：command+option+n

15、[LESS](https://packagecontrol.io/packages/LESS)

功能：less语法高亮

使用：打开.less文件或者设置为less格式

16、[ConvertToUTF8](https://packagecontrol.io/packages/ConvertToUTF8)

功能：文件转码成utf-8,可以编辑并保存目前编码不被 Sublime Text 支持的文件，特别是中日韩用户使用的 GB2312，GBK，BIG5，EUC-KR，EUC-JP ，ANSI等。ConvertToUTF8 同时支持 Sublime Text 2 和 3

使用：安装插件后自动转换为utf-8格式

17、[Sublime​Linter](https://packagecontrol.io/packages/SublimeLinter)

功能：代码检测
使用：此插件依赖nodejs,并且本机需全局安装jshint、csslint,然后再看着sublimelinter-jshint以及sublimelinter-csslint,然后再配置sublimelinter配置文件后，重启sublime后生效，配置注意点：

        "paths": {
            "linux": [],
            "osx": [
                "/Users/sutengfei/.nvm/versions/node/v6.11.5/bin"
            ],
            "windows": []
        },
        
根据自己的系统，配置自己node安装目录，保存，重启后生效。

18、[CSScomb](https://packagecontrol.io/packages/CSScomb)

功能: css排序

使用: 选中需要排序的css(连同选择器选中，否则会无效，控制台会报错)

配置: 此插件依赖nodejs
		
		{
		  "node-path" : ":/Users/sutengfei/.nvm/versions/node/v6.11.5/bin",
		}
###常用快捷键

cmd+shift+p 调出命令面板

Command + T：查询/前往文件

Command + R：查询/前往funcdtion或method

Command + K + B: 隐藏/显示边栏

Command + L：选择当前光标整行

Command + D：选择当前光标所在的一个词 （继续按会继续选取下一个同样的词）

Ctrl + Shift + K: 删除当前行

Command + K + U: 转换为大写

Command + K + L: 转换为小写

Comamand+ Shift + V: 粘贴并缩进

Command + F：查找

Command + Shift + F：查找替换

Command + / : 注释/非注释

Command + W 关闭页面

Ctrl + M：前往匹配的括号

Ctrl + G 跳转到对应行号

Ctrl + Tab 切换到下一个页面

Ctrl+ Shift + Tab 切换到上一个页面

Command +⬅️ 光标定位到当前行最前 + Shift 选中

Command +➡️ 光标定位到当前行最后 + Shift 选中

Command +⬇️ 光标定位到当前页最后 + Shift 选中

Command +⬆️ 光标定位到当前页最前 + Shift 选中

###写在最后的话

sublime本身并不强大，强大的是它的思路，每个人都可以根据自己的需求，配置出一个合适自己风格的sublime。

有句话说的好，没有什么功能是sublime没有的，如果有，那就再装个插件，如果还是满足不了你的需求，那就自己写一个。
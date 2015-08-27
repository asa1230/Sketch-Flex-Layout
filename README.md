# sketch 自适配布局插件
安装插件：
	-1.下载包里的ZIP文件                                                                           
	-2.双击“Flex-Layout.sketchplugin”文件，完成安装.                                                     
	
**重要提示 :** *这里是一个早期测试的版本. 许多功能还要大家熟悉后，才能更好使用。前期请大家不要立即重要的项目中来使用它.*

![](http://i.imgur.com/Z5A8Hqo.png)

插件使用主要包含2个部分，CSS文件和布局模版.布局模版是抽象过了的界面元素。如果大家不太好理解的话，建议先下一个 [案例](https://github.com/hrescak/Sketch-Flex-Layout/raw/master/ExampleFile.sketch) 来进一步了解和掌握插件的工作原理

##写样式表文件

![](http://i.imgur.com/2FcoADp.png)

1. 创建一文本图层并命名为 **“@stylesheet”**.
2. 撰写CSS的一些规则:
	- 了解支持的属性及清单请看 [这里](https://github.com/facebook/css-layout).
	- 使用骆驼命名方法
	- 不需要写单位
	- 暂时还不能支持缩写快速编码输入
	- 只能写CLASS名称，不能写ID *(.something)*
	- 没有嵌套样式 *(“\>” declarations)*
3. 创建一些图层并修改命名. 比如你样式写的是 '.someclass{width:200;}', 你需要修改你的图层名'Rect1' 为 'Rect1 .someclass'
4. 使用 cmd + ctrl + L 快捷键可以运行效果 _(确定你的css样式层没有被选择, 不然的话 你的效果无法看得到；请检查你的快捷键，保证快捷键没有被占用)_

## 使用模版

![](http://i.imgur.com/Y86vIYJ.png)

1. 创建一个图层组并命名为 **"prototype .SOMETHING"**
2. 添加一些矩形来定义或描述UI的风格 - [支持的命名后缀和功能](http://i.imgur.com/IguIeFI.png)
	- 如果你需要，可以新增一文本图层命名为 **"@styles"** 用分好风格开 - [支持的样式和属性](http://i.imgur.com/oseZ1Dr.png)
3. 你可以用UI元素模版创建更多UI元素, 可以不用跟上模版的后缀名，比如 **".somethingelse"** 这样的命名就好了。
4. 点击运行 _Add Object From Prototype_ 命令菜单 - 这个将复制模版, 移除所有图层样式层。如果你有图层样式层的话，
他也会将图层组移到图层的底部。
5. 做完所有工作后,运行 cmd + ctrl + L 会看到效果了.

**提示** - 在一个画布中，可以同时存在一个模版或命名为*@stylesheet*的图层.

**专业提示** - 当你复制你的图层组的时候, 你可以去掉sketch自动添加的 "copy"后缀 - 点击设置 > Layers > 不点选 "Rename Duplicated Layers"

## 提示

1. 在每个画布都可以有不同的样式表文件。样式文件只对当前的文件有效。
2. 如果一个图层组有样式文件，所有组内文件都遵循该样式.
3. 添加一个名为 **"bg"** 的层在你的组.因为这里不像html，每个效果层不一定有背景.
4. 图层命名最好与“ page”  “prototypes”等系统名称区分开 .不同模版或不同样式表中的“picture, 只有一个会得到应用.

## 即将做的 / 已知问题

- 查看 [问题1](https://github.com/hrescak/Sketch-Flex-Layout/issues) .

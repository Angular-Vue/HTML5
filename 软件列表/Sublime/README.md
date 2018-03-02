# Sublime插件安装 #
#### 1. Package Control,必装.是装其他插件的工具

#### 按``ctrl+` ``打开sublime命令行或者View > Show Console，输入：

import urllib.request,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)


#### 重启sublime,完成安装
#### 以下插件均是按下快捷键  Ctrl+shift+P 后,输入  install package  ,再搜索 插件名称 安装
| 插件名称              | 插件介绍                             |
|--------------------|--------------------------------------|
| sidebarEnhancements       | 文件夹选项扩展 只有**sublime 3**有                     |
| Git             | Sublime集成git的插件                        |
| WordHighlight             | 顾名思义,高亮相同与你选择的字符串                            |
| JavaScriptNext             | JS语法高亮,支持ES6语法                        |
| emmet      | 用于html和twig文件的快速编写                        |
| less       | less语法高亮                            |
| jQuery             | 在编写jQuery的时候，给出语法提示     |

####  一些常用的快捷键 ####

| 快捷键              | 快捷键介绍                             |
|--------------------|--------------------------------------|
| Ctrl+Shift+P       | 打开命令面板                           |
| Ctrl+P             | 搜索项目中的文件                        |
| Ctrl+G             | 跳转到第几行                            |
| Ctrl+W             | 关闭当前打开文件                        |
| Ctrl+S hift+W      | 关闭所有打开文件                        |
| Ctrl+Shift+V       | 粘贴并格式化                            |
| Ctrl+D             | 选择单词，重复可增加选择下一个相同的单词     |
| Ctrl+L             | 选择行，重复可依次增加选择下一行            |
| Ctrl+Shift+L       | 选择多行                                |
| Ctrl+Shift+Enter   | 在当前行前插入新行                       |
| Ctrl+X             | 删除当前行                              |
| Ctrl+M             | 跳转到对应括号                           |
| Ctrl+U             | 软撤销，撤销光标位置                      |
| Ctrl+J             | 选择标签内容                            |
| Ctrl+F             | 查找内容                               |
| Ctrl+Shift+F       | 查找并替换                              |
| Ctrl+H             | 替换                                   |
| Ctrl+R             | 前往 method                            |
| Ctrl+N             | 新建窗口                               |
| Ctrl+K+B           | 开关侧栏                               |
| Ctrl+Shift+M       | 选中当前括号内容，重复可选着括号本身        |
| Ctrl+F2            | 设置/删除标记                           |
| Ctrl+/             | 注释当前行                              |
| Ctrl+Shift+/       | 当前位置插入注释                         |
| Ctrl+Alt+/         | 块注释，并Focus到首行，写注释说明用的       |
| Ctrl+Shift+A       | 选择当前标签前后，修改标签用的             |
| F11                | 全屏                                   |
| Shift+F11          | 全屏免打扰模式，只编辑当前文件             |
| Alt+F3             | 选择所有相同的词                        |
| Alt+.              | 闭合标签                               |
| Alt+Shift+数字      | 分屏显示                               |
| Alt+数字            | 切换打开第N个文件                       |
| Shift+右键拖动       | 光标多不，用来更改或插入列内容            |
| 鼠标的前进后退键       | 可切换Tab文件                         |
| 按Ctrl，依次点击或选取 | 可需要编辑的多个位置                    |
| 按Ctrl+Shift+上下键   | 可替换行                             |

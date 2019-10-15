# Markdown教程
## 简介
Markdown是一种轻量级**标记语言**，具有轻量化、易读易写的优点，支持图片、图表及数学式等，许多网站广泛支持Markdown格式显示，如**Github**、reddit、简书等。

## 步骤
1. 学习Markdown的语法，请参考[Markdown基本语法](https://www.jianshu.com/p/191d1e21f7ed)。
2. 选择一种编辑器进行文档编辑，这里推荐[Visual Studio Code](https://code.visualstudio.com/Download) 编辑器。使用该编辑器进行文档编写，编写后将文件命名为“文件名.md”的形式。（该编辑器可以实时预览显示效果，请参考[VS Code 实时预览方法](https://www.cnblogs.com/shawWey/p/8931697.html)）。
3. 最终编辑后得到文件“文件名.md”，该文件内容即可在github里直接显示，或者通过**Pandoc**转换为PDF或HTML等其他格式。

# Pandoc教程
## 简介
Pandoc是**标记语言**转换工具，可实现不同标记语言间的格式转换，堪称该领域中的“瑞士军刀”。Pandoc以**命令行**形式实现与用户的交互，可支持多种操作系统。

Pandoc支持的标记语言格式如下表：

Pandoc可读取的原格式    |   Pandoc可生成的目标格式  
:-|:-
Markdown|HTML格式：包括XHTML，HTML5及HTML slide
reStructuredText|文字处理软件格式：包括docx、odt、OpenDocument XML
textile|电子书格式：包括EPUB（第2版及第3版）、FictionBook2
HTML|技术文档格式：包括DocBook、GNU TexInfo、Groff manpages、Haddock
DocBook|页面布局格式：InDesign ICML
LaTeX|大纲处理标记语言格式：OPML
MediaWiki标记语言|TeX格式：包括LaTeX、ConTeXt、LaTeX Beamer
OPML|PDF格式：需要LaTeX支持
Org-Mode|轻量级标记语言格式：包括Markdown、reStructuredText、textile、Org-Mode、MediaWiki标记语言、AsciiDoc
Haddock|自定义格式：可使用lua自定义转换规则

## 安装
### Windows平台
下载[安装包](https://pandoc.org/installing.html#windows)并执行安装程序

### Linux平台
Pandoc 已经被集成到系统的软件源内，可直接从软件源安装：

```
sudo apt-get install pandoc
```

## 使用
### Windows平台
打开**cmd**，通过**cd**指令进入pandoc安装目录下，并将要转换的文件放在这个目录下。然后在命令行中输入pandoc命令（见下）。

### Linux平台
打开终端窗口，输入pandoc命令(见下)。

### Pandoc命令
Pandoc官方命令手册见 [Pandoc User's Guide](https://pandoc.org/MANUAL.html#option--standalone)

常用命令如下：

命令均为：“pandoc + 参数 ”的形式
```
pandoc -o output.html input.txt

-o: 输出到文件output.html
```
上式命令为：将输入文件input.txt转换生成为output.html，原输入文件会保留

```
pandoc -f markdown -t latex hello.txt

-f: 指定输入格式(from)，比如docx、epub、md、html等

-t: 指定输出格式(to)，比如docx、epub、md、html等
```
上式命令为：将hello.txt以markdown格式输入，转换为latex格式

还有其他参数如下：
```
-v: 打印版本信息

-h：显示语法帮助

--verbost: 显示详细调试信息

--log：指定输出日志信息

--list-input-formats：列出支持的输入格式

--list-output-formats：列出支持的输出格式

--list-extensions：列表支持Markdown扩展，后面跟一个+或者-说明是否在pandoc的Markdown中默认启用

--list-highlight-languages:列出语法突出显示支持的语言

--list-highlight-styles:列出支持语法高亮的样式。
```

$$ f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right) $$

参考[guoyuchaun](./guo.rst)


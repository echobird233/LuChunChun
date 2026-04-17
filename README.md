# LuChunChun LaTeX 数学笔记模板使用说明

LuChunChun 是一个 LaTeX 数学笔记模板，通过预定义的样式和命令，用于生成具有统一格式的笔记文档。以下是该模板的功能及调用方式介绍。

## 1. 预置宏包

模板已内置常用的 LaTeX 宏包，用户无需在主文档中使用 `\usepackage` 重新调用，可直接使用以下功能：

* **中文排版与字体**：`ctex` `fontspec`
* **数学支持**：`amsmath` `amsthm` `amssymb` `mathrsfs`
* **图片与绘图**：`graphicx` `adjustbox` `float` `tikz`
* **页面布局与格式**：`geometry` `fancyhdr` `lastpage` `titlesec` `tocloft` `caption`
* **色彩与文本框**：`xcolor` `tcolorbox`
* **交叉引用**：`hyperref`

## 2. 页面与排版设定

* **字体**：中文字体、无衬线字体及等宽字体均默认指向同级目录下的仓耳今楷01W03.ttf文件。
* **页面规格**：A4 纸张，上下左右页边距均设定为 2.5 厘米。
* **层级显示**：目录深度（tocdepth）设置为 2，显示至 subsection 层级。
* **正文页脚**：左侧显示副标题，右侧显示“第 X 页 丨 共 Y 页”。

## 3. 文档信息配置与页面生成

通过在导言区调用以下命令，可以配置文档变量：

* `\title{主标题内容}`：设置主标题
* `\subtitle{副标题内容}`：设置副标题
* `\author{作者姓名}`：设置作者信息
* `\contact{联系方式}`：设置联系信息
* `\setsectionimage{图片文件名}`：配置封面和 Section 章节背景图（默认：covers.png）

在正文环境之后使用以下命令生成预设页面：

* `\makecover`：生成带背景和排版的封面页（需确保存在背景图文件及 character.png 装饰图）。
* `\makeTOC`：生成带有特定背景样式的目录页（需确保存在 content.png 图片文件）。

## 4. 数学环境调用

模板预先定义了 4 个数学环境。这些环境支持跨页自动断行，按section自动编号，并使用独立设定的配色方案。调用方式统一如下：

* **定义（深蓝色框体）**：
    ```latex
    \begin{定义}[可选标题内容]
    正文内容...
    \end{定义}
    ```
* **定理（浅蓝色框体）**：
    ```latex
    \begin{定理}[可选标题内容]
    正文内容...
    \end{定理}
    ```
* **引理（粉色框体）**：
    ```latex
    \begin{引理}[可选标题内容]
    正文内容...
    \end{引理}
    ```
* **例题（紫色框体）**：
    ```latex
    \begin{例题}[可选标题内容]
    正文内容...
    \end{例题}
    ```

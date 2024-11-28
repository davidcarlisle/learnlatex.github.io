---
layout: "lesson"
lang: "zh-hans"
title: "基本的 LaTeX 文档结构"
description: "本课展示了 LaTeX 文档的基本结构，以及如何将其构建为PDF文件，还介绍了用于控制 LaTeX 的主要特殊字符。"
toc-anchor-text: "文档结构"
toc-description: "文档的基本结构。"
---

# LaTeX文档结构

<span
  class="summary">本课展示了 LaTeX 文档的基本结构，以及如何将其构建为PDF文件，还介绍了用于控制 LaTeX 的主要特殊字符。</span>

你的第一个 LaTeX 文档将非常简单：目的是向你展示文档的外观以及如何成功排版。这也是你第一次看到如何在`learnlatex.org`上使用示例。

如果你使用的是本地 LaTeX 安装，请在编辑器中创建一个名为`first.tex`的新文件，并复制粘贴下面的文本或手动输入。

如果你使用的是在线系统，只需点击示例中的“在 TeXLive.net 运行”或“在 Overleaf 中打开”按钮即可试用！

<p
  class="hint">我们建议你即使已经在本地设置了 LaTeX，也尝试在线选项；这是一个了解不同选项如何工作的好机会。</p>

```latex
% !TEX program=lualatex

\documentclass{ctexart}

\begin{document}
Hello, world!

这是一个简单的中英文混排文档。
\end{document}
```

<p class="hint">当你使用 ctexart（或其他ctex文档类）时，无需加载 xeCJK 宏包（`\usepackage{xeCJK}`）。现代TeX引擎会根据需要自动加载对应的CJK宏包，简单的 ctexart 文档应该在所有引擎上都能正常工作。在编译 LaTeX 文档时最好使用 LuaLaTeX 引擎，不仅因为它在处理大型文档时更快，而且它是被推荐的编译引擎(https://www.texdev.net/2024/11/05/engine-news-from-the-latex-project)。</p>

保存文件并将其排版为PDF文档；如果你使用的是本地 LaTeX 安装，具体的按钮取决于你选择的编辑器。你应该会得到一个包含上述文本 _加上_ 页码的PDF文件；LaTeX 会自动添加页码。

使用你喜欢的PDF查看程序查看输出`first.pdf`。看起来不错，恭喜！

如果你想获得HTML而不是PDF输出，请查看[帮助](./help)以了解如何实现。

## 处理错误

错误是难免的。检查你是否准确输入了文本文件中的每一行。有时看似微小的输入更改会导致结果发生巨大变化，包括导致文档无法工作。如果你遇到困难，请尝试擦除文档并从上面的行中重新复制。

如果你的 LaTeX 排版运行以问号结束，你可以通过输入`x`和`<Enter>`退出。

LaTeX 的错误消息试图提供帮助，但它们与文字处理器中的消息不同。有些编辑器也使得很难看到错误的“完整”文本，这可能会隐藏关键细节。LaTeX 总是会创建一个以`.log`结尾的日志文件，记录它正在做的事情。你总是可以在那里看到完整的错误消息，如果你遇到问题，LaTeX 专家通常会要求你提供日志文件的副本。

我们在[第15课](./lesson-15)中介绍了更多关于处理错误的内容。

## 你已经掌握的知识

- 第一个文档展示了基础知识。LaTeX 文档是文本和命令的混合。命令以反斜杠开头， 有时在大括号中有参数，（有时在方括号中有可选参数）。然后通过告诉 LaTeX 排版你的文件来获得输出PDF。

- 每个 LaTeX 文档都有一个`\begin{document}`和一个匹配的`\end{document}`。这两者之间是*文档主体*，你的内容放在这里。这里的主体有两段（在 LaTeX 中，你可以通过一个或多个空行分隔段落）。
- 在`\begin{document}`之前是*文档前言*，其中有设置文档布局的代码。`\usepackage`命令在[后面的课程](lesson-06)中描述，在本网站的大多数示例中使用它来设置字体编码。

- LaTeX 还有其他的`\begin{...}`和`\end{...}`对；这些被称为*环境*。你必须匹配它们，以便每个`\begin{x}`都有一个`\end{x}`。如果你嵌套它们，那么你必须有`\end{y} ... \end{x}`来匹配`\begin{x} ... \begin{y}`，即`begin`和`end`语句按顺序匹配。

我们可以通过以`%`开头在 LaTeX 文件中添加注释；让我们看个例子：

```latex
% !TEX program=lualatex

\documentclass{ctexart} % 带选项的文档类
% 前言中的注释
\begin{document}
% 这是一个注释
这是一个简单的文档\footnote{带有脚注}。

这是一个新段落。
\end{document}
```

你可以在上面看到我们有两段：注意使用空行来实现这一点。还要注意多个空格被视为一个空格。

你可能还希望有时使用“硬”空格，不会在行间断开：在 LaTeX 中，我们可以使用`~`来创建，将两个文本片段“绑”在一起。这在我们稍后开始创建交叉引用时特别有用。

## 特殊字符

你可能已经注意到``\``、`{`和`}`对 LaTeX 有特殊意义。
``\``开始一个LaTeX指令：一个“命令”。大括号字符`{`和`}`用于表示_必需参数_：命令所需的信息。

还有一些其他字符具有特殊意义；我们刚刚看到`~`是一个“硬”空格。例如。几乎所有这些字符在普通文本中都非常不常见，这就是为什么它们被选择为特殊含义的原因。
如果你确实需要显示这些特殊字符之一，我们在[详细信息页面](more-03)中提供了一些信息。

## 练习

尝试使用在线编辑和排版系统；点击按钮排版内容，然后在网页中编辑并重新排版。

尝试向你的第一个文档添加文本，排版并查看PDF中的更改。制作一些不同的段落并添加可变空格。探索你的编辑器如何工作；点击你的源文件并找到如何在PDF中转到同一行。尝试添加一些硬空格并查看它们如何影响换行。
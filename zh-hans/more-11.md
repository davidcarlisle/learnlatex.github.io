---
layout: "lesson"
lang: "zh-hans"
title: "更多内容：格式：字体和间距"
description: "本课展示了如何抑制单个段落的缩进。"
toc-anchor-text: "更多内容：格式：字体和间距"
---

## 抑制单个段落的缩进

如果你想抑制单个段落的缩进，可以使用`\noindent`命令。
这种用法应该 _非常_ 少见；大多数时候，你应该让 LaTeX 自动处理这个问题。

```latex
% !TEX program=lualatex

\documentclass{ctexart}
\begin{document}
一个小段落，我们稍微填充一些内容以确保你能在这里看到效果！

一个小段落，我们稍微填充一些内容以确保你能在这里看到效果！

\noindent 一个小段落，我们稍微填充一些内容以确保你能在这里看到效果！
\end{document}
```

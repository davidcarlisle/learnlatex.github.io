---
layout: "tagging"
lang: "en"
title: "Tagging with LaTeX"
description: "This lesson shows the basic decarations needed for Tagged PDF in a LaTeX document."
toc-anchor-text: "Tagged Document structure"
toc-description: "The basic declarations for tagged PDF."
---

# LaTeX document structure

<span
  class="summary">This lesson shows the basic declarations needed to generate Tagged PDF with LaTeX.</span>

Your first Tagged PDF LaTeX document is going to be very simple: the idea is to show you
how a document looks and how to typeset it successfully. It is also your
first chance to see [how to use the examples](help) here on `learnlatex.org`.

If you are using a local LaTeX installation, in your editor create a new file
called `first.tex`, and either copy–paste the text below or type it in.

If you are using the online system, you can just click on the 'Generate Tagged PDF' button
to generate the PDF at  TeXLive.net.

<p
  class="hint">We suggest you try out the online options even if you have set up LaTeX locally; this is a good chance to see how the different options work.</p>

```latex
\DocumentMetadata{
 tagging=on,
 pdfstandard=ua-2,
 tagging-setup={math/setup=mathml-SE} %or mathml-AF
}
\documentclass{article}
\usepackage{unicode-math}
\title{Tagging Prototype}
\begin{document}

\section{Example}
Some text
\begin{itemize}
\item one
\item two
\end{itemize}
\[
ax^2+b^x+c=0
\]
\end{document}
```

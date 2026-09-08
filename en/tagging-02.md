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
  class="summary">This lesson shows the basic structure of a LaTeX document, and how to build it into a PDF file, as well as the main special characters used to control LaTeX.</span>

Your first LaTeX document is going to be very simple: the idea is to show you
how a document looks and how to typeset it successfully. It is also your
first chance to see [how to use the examples](help) here on `learnlatex.org`.

If you are using a local LaTeX installation, in your editor create a new file
called `first.tex`, and either copy–paste the text below or type it in.

If you are using the online system, you can just click on the ‘Run at TeXLive.net’
or ‘Open in Overleaf’ buttons in the example to try it out!

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

Save the file and typeset it to a PDF document; if you are using a local LaTeX
installation, the exact button to press will depend on the editor you have
picked. You should get a PDF file that contains the text above _plus_ a page
number; LaTeX adds that automatically.

View the output `first.pdf` with whatever program you prefer for PDF viewing.
Looks great; congratulations!

If you want to get HTML rather than PDF output, take a look at the
[help](./help) for how you can do that.

## Exercise

Experiment with the online editing and typesetting system; click the
button to typeset the content, then edit it in the webpage and re-typeset it.

Try adding text to your first document, typesetting and seeing the changes in
your PDF. Make some different paragraphs and add variable spaces. Explore how
your editor works; click on your source and find how to go to the same line  in
your PDF. Try adding some hard spaces and see how they influence line-breaking.

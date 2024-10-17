---
title: "extex"
excerpt: "LaTeX extraction tool: compile TeX files (like tikz pictures or equations) to standalone pdf and svg files. "
collection: coding
gitlink: 'https://github.com/baronefr/extex'
date: 2024-10-15
---

<br>

`extex` is a LaTeX extractor: it takes batches of input files and compiles them to pdf with tight page layout.
Additionally, the pdf file can be exported to svg.

<img src='https://raw.githubusercontent.com/baronefr/extex/refs/heads/main/img/cover.svg' class='page__image-large'>

The original **purpose** of this utility is to **compile batches of tikz pictures to pdf**, avoiding the overhead of compiling them from scratch in a full-scale project. 
Furthermore, the utility allows to **export the tikz pictures as svg files**, which can be imported in PowerPoint documents - or any other document that does not support pdf input.
Even though these are two prominent application examples, I am sure that you might find other creative ways of putting it to use.

To assure the best compatibility, **the LaTeX preamble is entirely customizable**. 
You might even use the same `main.tex` file of your source project: `extex` will take care of removing the document content (without touching your file) and use its preamble to compile the input files. 
This ensures the best rendition of the output, as it will use the same settings of your preamble/custom class.


### Requirements

* Linux-based OS.
* A **working LaTeX installation**. The script should be able to access a compiler (pdflatex/xelatex or any custom binary that can be specified via option).
* **[pdf2svg](https://archlinux.org/packages/extra/x86_64/pdf2svg/)** (optional) for svg conversion.

<br>

## How does it work

Suppose to have a LaTeX project like the one in the [`example/`](https://github.com/baronefr/extex/tree/main/example) folder.
The [compiled document](https://raw.githubusercontent.com/baronefr/extex/refs/heads/main/example/main.pdf) shows two tikz figures and one equation, along with some text. 
The pictures and the equation are defined by TeX files placed in the directory `inputs/`, which are taken as input in the document `main.tex` file.

A run of `extex` iterates over all the TeX source files in the directory `inputs/`, combines them with the preamble of `main.tex`, and compiles each file to a separate pdf or svg file. Check out the outputs in `example/extex-pdf` (`example/extex-svg`).

```bash
cd example/
extex inputs/ --svg --preamble main.tex
```
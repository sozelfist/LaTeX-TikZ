# LaTeX-TikZ

📚 This is a repository for storing and sharing **LaTeX-TikZ**  and **PGFPlots** pictures.

## Usage

```sh
# clone the repo
$ git clone https://github.com/TruongNhanNguyen/LaTeX-TikZ.git
# navigate to specify folder
$ cd <folder-name>
# example
# cd TikZ/GitHubProfilePicture
# compile .tex to .pdf
$ pdflatex main.tex
```

## My Github Profile Picture

![github](TikZ/GitHubProfilePicture/github-profile-picture.png)

```latex
\documentclass[tikz, border=10pt]{standalone}

\usepackage{tikz}
\usetikzlibrary{trees, snakes}
\usepackage{xcolor}

\tikzset{
    level 1/.style = {sibling angle=120},
    level 2/.style = {sibling angle=60},
    level 3/.style = {sibling angle=30},
    every node/.style = {fill},
    edge from parent/.style = {snake=expanding waves, segment length=1mm, segment angle=10, very thick, draw}
}

\begin{document}
    \begin{tikzpicture}[grow cyclic, shape=circle, level distance=13mm ,cap=round]
        \node {} child [color=\A] foreach \A in {red, green, blue} {
            node{} child [color=\A!50!\B] foreach \B in {red, green, blue}{
                node{} child[color=\A!50!\B!50!\C] foreach \C in {black, gray, white}{
                    node{}
                }
            }
        };
    \end{tikzpicture}
\end{document}
```

## Language and Tools

[![windows](https://img.shields.io/badge/windows-11-blue?logo=windows&logoColor=blue&labelColor=000000)](https://www.microsoft.com/en-us/windows?r=1)
[![git](https://img.shields.io/badge/Git-2.34.1.windows.1-f05032?logo=git&labelColor=000000)](https://git-scm.com/)
[![github](https://img.shields.io/badge/GitHub-000000?logo=github&logoColor=181717&labelColor=white)](https://github.com)
[![VSCode](https://img.shields.io/badge/Visual_Studio_Code-1.63.2-1f425f.svg?logo=visual-studio-code&logoColor=007acc&labelColor=000000)](https://code.visualstudio.com/)
[![texlive](https://img.shields.io/badge/TeXLive-2021-teal?logo=latex&logoColor=teal&labelColor=000000)](https://tug.org/texlive/)
[![latex-workshop](https://img.shields.io/badge/latex_workshop-8.23.0-007acc?logo=visual-studio-code&logoColor=007acc&labelColor=000000)](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

## My LaTeX Workshop extensions `.config`

I placed all settings of **LaTeX Workshop** ext here
[`latex-workshop.json`](.config/latex-workshop.json)

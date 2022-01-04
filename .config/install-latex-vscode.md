# LaTeX on Visual Studio Code

##  Do you want to write LaTeX on VSCode

When we talk about LaTeX editing, people would mention **TeXstudio**, **WinEdt** or **TeXMaker** with ***MiKTeX*** or ***TeX Live***. For a long time, **Overleaf** was my one and only editor (online LaTeX editor). But as time I want to work locally on my computer, so I switched to the open-source, feature-rich VSCode.

> I  will show you how to write LaTeX documents using VSCode and live-preview its PDF output inside VSCode, as well as use SyncTeX to sync cursors between input and output of the LaTeX document.
>
> ***Note***: This article demonstrates the process in Windows, but you can use the same tools on Linux with just a few small modifications.

## 🎯 Install TeXLive 2021

I prefer ***TeX Live*** over other distribution like ***MiKTeX***, ***W32TeX*** or **MacTeX** (only for MacOS), not just because it has more secure default values and well-maintained but also because it contains everything (packages, tools, ...) a regular user need when it comes to a TeX distribution. But you can use any other TeX distribution to your LaTeX writing.

I recommend starting the TeX Live installation by downloading [install-tl.zip](https://tug.org/texlive/acquire-netinstall.html) (~25mb). Detailed installation steps is available on [TeX Live homepage](https://tug.org/texlive/).

## 🎯 Install LaTeX Workshop extension

LaTeX Workshop is the only extension that you need for LaTeX typesetting with VSCode.

In order to install LaTeX Workshop, launch VSCode and go to the extension tab to search for it (`Ctrl+Shift+X`). Then, just click `install` to install the extension.

LaTeX-Workshop provides a smooth LaTeX experience, thanks to its long list of features:

- Build LaTeX (including BibTeX) to PDF automatically on save.
- Preview PDF in realtime side-by-side in VS Code or a PDF viewer.
- Direct and reverse SyncTeX. You can jump between any location in .tex source file and the corresponding PDF file and vice versa.
- Intellisense integrated, autocomplete for bibliography keys `\cite{}` and labels `\ref{}`.
- LaTeX errors and warnings shown inside VS Code.
- Keyboard combination for quick text formatting.

## 🛠️ Configure LaTeX Workshop in VSCode

The first thing you need to do is set up LaTeX command line tool to work with LaTeX Workshop.

To do that, open the **command Palatte**, find **Open settings (JSON)** and put all settings in the [`latex-workshop.json`](latex-workshop.json) (my standard configs of LaTeX Workshop) into `setting.json`.

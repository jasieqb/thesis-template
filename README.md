# UMCS thesis template
## Contains:
* multi-file latex project
* BibLaTeX for [bibliography](refs.bib)
* [devcontainer](.devcontainer/devcontainer.json) preconfigured for vscode
* auto build pdf with Github Actions (each commit)

## How to use
* template this repo (button on top right)
* clone your repo
* open in vscode
* install [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
* open command palette (`ctrl+shift+p`) and select `Remote-Containers: Reopen in Container`
* open [`thesis.tex`](thesis.tex) and build pdf
* edit [`refs.bib`](refs.bib) and [`thesis.tex`](thesis.tex) by your needs :)

## Use without vscode
On ubuntu/debian:
```bash
sudo apt-get update && sudo apt-get install -y texlive-base texlive-lang-polish texlive-extra-utils texlive-latex-recommended chktex latexmk texlive-bibtex-extra biber
```
Propably you will need to install some more packages, but this is the basic set.


Then (to build pdf):
```bash
latexmk -synctex=1 -interaction=nonstopmode -file-line-error -pdf -shell-escape -bibtex thesis.tex
```
You can also use `latexmk` with you favorite LaTeX editor.

## TODO 
* imporve ci/cd:
  * auto release by tags  

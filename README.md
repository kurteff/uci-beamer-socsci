# uci-beamer-socsci
Unofficial Beamer Template for UCI School of Social Sciences

The starting point for this template was the [Unofficial UCI Engineering Beamer Template](https://www.overleaf.com/latex/templates/unofficial-uci-engineering-beamer-template/qvqfvsctgkgn). However, I'm in the Cognitive Sciences department so I needed one for my school. I also drew inspiration from [sajjadt's unofficial UCI template](https://github.com/sajjadt/uci-beamer).

## Usage
You have several options on how to use this theme, all start with cloning the repo:
```
git clone https://github.com/kurteff/uci-beamer-socsci.git
```
For additional guidance on usage, please see `example.tex`.

## Installation
You can just use this theme in a local project directory, but if you plan to use it for many presentations then installing it to your `texmf` folder is the way to go.

The first step is to identify where your TeX distribution expects to see this folder. For macOS, it's usually `~/Library/texmf`, but for Linux it could be simply in `~/texmf`. Then, copy the files from the repo to that folder (example is for macOS):

```
mkdir -p ~/Library/texmf/tex/latex/beamer/themes/UCI-socsci
cp -r ./theme/ ~/Library/texmf/tex/latex/beamer/themes/UCI-socsci/
mktexlsr ~/Library/texmf
```

`kpsewhich beamerthemeUCI-socsci.sty` can help with troubleshooting and should return `/Users/<<your username>>/Library/texmf/tex/latex/beamer/themes/UCI-socsci/beamerthemeUCI-socsci.sty` if your paths are configured properly.


_(Note: if you are having issues with paths, configuring `beamerthemeUCI-socsci.sty` to use absolute paths instead of relative ones miiiight help)_

### For Sublime Text / LaTeXTools users
You will have to configure your `LaTeXTools.sublime-settings` file. This is a pain and varies pretty largely by OS so I leave it as an exercise to the reader. :)

Here's what worked for me (macOS Sequoia 15.5):

```
// Settings in here override those in "LaTeXTools/LaTeXTools.sublime-settings"
{
    "texpath": {
        "osx": "/Library/TeX/texbin"
    }
}
```
# uci-beamer-socsci
Unofficial Beamer Template for UCI School of Social Sciences

The starting point for this template was the [Unofficial UCI Engineering Beamer Template](https://www.overleaf.com/latex/templates/unofficial-uci-engineering-beamer-template/qvqfvsctgkgn). However, I'm in the Cognitive Sciences department so I needed one for my school. I also drew inspiration from [sajjadt's unofficial UCI template](https://github.com/sajjadt/uci-beamer).

## Usage
You have several options on how to use this theme, all start with cloning the repo:
```
git clone https://github.com/kurteff/uci-beamer-socsci.git
```
For additional guidance on usage, please see `example.tex`.

#### Option 1. Local import
Copy and paste the `theme` folder to any project you want to use this theme in. Easy peasy.

_(Note: if you are having issues with paths, configure line 26 of `beamerthemeUCI-socsci.sty` so that it is an absolute path instead of `\file@path`.)_

#### Option 2. Add theme folder to bash profile
...I would suggest adding an export to your bash profile. For MacOS users this is going to be located at `~/.zshrc` and for most Linux users it will be `~/.bashrc`:
```
# Add to bash profile
# Please be sure to update /path/to/uci-beamer-socsci !
echo "export TEXINPUTS=\$HOME/path/to/uci-beamer-socsci/theme//:" >> ~/.zshrc
```
Then, using the theme is as simple as `\usepackage[widescreen]{beamerthemeUCI-socsci}` at the start of your `.tex` file.  :)

#### Option 3. "Install" theme to your TeX tree
```
# Point bash to your texmf folder
`echo "export TEXMFHOME=$HOME/texmf" >> ~/.zshrc`
# Change dir to the folder you cloned
cd ./uci-beamer-socsci
# Copy files to your local TeX install
mkdir -p ~/texmf/tex/latex/uci-beamer-socsci
cp -r ./theme/* ~/texmf/tex/latex/uci-beamer-socsci/
# Update the filename database (if needed)
mktexlsr ~/texmf
```
Usage after this is the same as Option 2.

#### For Sublime Text / LaTeXTools users
You will have to configure your `LaTeXTools.sublime-settings` file. This is a pain and varies pretty largely by OS so I leave it as an exercise to the reader. :)

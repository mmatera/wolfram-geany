# wolfram-geany

This is a [Wolfram Language](https://en.wikipedia.org/wiki/Wolfram_Language) (WL) "plugin" for the [Geany](https://www.geany.org/) text editor editor based on UNIX-like systems (tested on Linux and MacOS)


### Features

1. Autocompletion
2. Documentation shortcuts (via _Context Action_)

### Dependencies
(All Platforms)

Download/Install [WolframCDFPlayer](https://www.wolfram.com/cdf-player) and [Wolframscript](https://www.wolfram.com/wolframscript)

#### Linux 
Be sure to have mlocate installed 
  `sudo apt-get install mlocate`

[zenity](https://gitlab.gnome.org/GNOME/zenity)
  `sudo apt-get install zenity`

#### MacOS

[brew](https://brew.sh/) 
  `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

[findutils](http://macappstore.org/findutils/) 
  `brew install findutils`

[zenity](http://brewformulas.org/Zenity)
  `brew install zenity`


## Installation

`wolframscript -f wolfram-geany.wl`


### Post-Installation

A colorscheme that fits pretty nicely is with the WL syntax is Kugel from the [Geany colorschemes](https://github.com/codebrainz/geany-themes)




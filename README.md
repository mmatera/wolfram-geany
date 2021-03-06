
# wolfram-geany

This is a [Wolfram Language](https://en.wikipedia.org/wiki/Wolfram_Language) (WL) plugin for the text editor [Geany](https://www.geany.org/) based on UNIX-like systems (tested on Linux and MacOS)


### Features

1. Autocompletion of WL built-in symbols
2. Documentation shortcuts (via [zenity](https://en.wikipedia.org/wiki/Zenity) and Geany [_Context Action_](https://www.geany.org/manual/current/#context-actions))

Watch a demo [here](https://www.youtube.com/watch?v=-IqsqBloF6k)


### Dependencies
(All Platforms)

Download/Install:

1. [Geany](https://www.geany.org/Download/Releases)
2. [WolframKernel](https://www.wolfram.com/cdf-player) + [Wolframscript](https://www.wolfram.com/wolframscript)

Run `$ wolframscript -configure` and set the variable `WOLFRAMSCRIPT_KERNELPATH` to your local `WolframKernel` address


#### Linux 

[Geany Plugins](https://plugins.geany.org/)
  `sudo apt-get install geany-plugins`

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

- Pick up a decent colorscheme like Kugel from the [Geany colorschemes](https://github.com/codebrainz/geany-themes)

- Configure documentation pop-up: go to _Edit->Preferences->Keybindings->Editor> Context Action_ and set a custom keybinding e.g. `Ctrl+h`. Once the keybinding is configured, press `Ctrl+h` to display the documentation of the built-in symbol under the cursor.

- The installation automatically configures Geany [_Execute_](https://www.geany.org/manual/current/#execute) to run a WL script by pressing F5. The script outputs can be displayed within the Geany [Virtual Terminal Emulator (VTE)](https://www.geany.org/manual/current/#virtual-terminal-emulator-widget-vte). As an alternative to the VTE, we suggest to install [urxvt](https://wiki.archlinux.org/index.php/rxvt-unicode), [rice it up](https://gist.github.com/ei-grad/3345657) and adjust Geany configuration to display the script outputs like so: go to _Edit->Preferences->Tools->Terminal_ and paste `urxvt -e /bin/sh %c`  

#### BUGS

On MacOS, evoking zenity from the _Context Action_ does not work, even though the very same command works if executed from the terminal. Please contribute! Thanks. 

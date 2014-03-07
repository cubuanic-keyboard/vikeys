vikeys
======

## Terminal user interface for configuring key mappings in keyboard firmwares.

[![vikeys](https://github.com/cjne/vikeys/raw/master/img/vikeys.png)](#features)


Inspired by vim it aims to make the editing a breeze.

***This is not complete at this stage, initial support for ErgoDox and the tmk firmware is almost there.***

###Currently supported keyboards
*  **ErgoDox** 

###Firmwares
*  [**TMK**](https://github.com/tmk/tmk_keyboard) Loading and saving of keymap.h files

Install
=======

***Note: This has only been tested on OS X so far***
This is a Node js application so the first thing you will need is NodeJS.

[Install node](http://nodejs.com)

In order to have any use for this tool you need the firmware and the dependencies for compiliing and upload the firmware to you keyboard controller.

[Get TMK firmware](https://github.com/tmk/tmk_keyboard)

[Get build dependencies](https://github.com/tmk/tmk_keyboard/blob/master/doc/build.md)

Finally, install vikeys: `npm install -g vikeys`

***For development and tweaking***
Instead of npm install, clone this repo and `ln -s /path/to/working/copy/vikeys.js /usr/local/bin/vikeys`

Usage
=====
cd to your firmware keyboard directory, for example:
`cd ~/tmk_keyboard/keyboards/ergodox`

You can load a keymap on start using:
`vikeys <name of keymap.h>`
or to just start vikeys with a blank keyboard.
`vikeys`

####Navigation
Vim keybindings are implemented wherever it makes sense, so you can use h, j, k and l to navigate, or use the arrow keys.
The main menu will have focus when you start vikeys, from there you can navigate to the various sections described below.
In the upper part of the screen you will see a visual representation of your keyboard. It will show what keys are mapped on the currently selected layer. You can change layer with the `+` and `-` keys.

####Modes
Upon start the mode is "Normal" which means the navigation keys will work in the lower half of the screen. It is possible to work on the keyboard part of the screen from normal mode using the shift key in combination with the navigation keys (vi only). So for example to select the next key to the right from normal mode, hold down shift and press `l`.

In order to use the regular arrow keys the mode can be changed to select mode. From normal mode press `Shift-s` or `i`. Press `Escape` to exit select mode. 

####Creating a new layout
Keyboards are defined in lib/keyboards.js, please send in a pull request if you want a new keyboard layout added.









# Commander ![CommanderSmallLogo](http://i.imgur.com/O7Aj373.png) [![shield](https://img.shields.io/badge/license-MIT-006969.svg?style=plastic)](http://opensource.org/licenses/MIT "MIT license")

![CommanderLogo](http://i.imgur.com/bDow6iB.png)

Commander is a portable & customizable workspace ready to use from minute one

## What does it include

* [**Cmder**](http://gooseberrycreative.com/cmder/) fully portable terminal emulator 
* [**Portable Python**](http://portablepython.com/) Interpreter
* [**Sublime Text**](http://www.sublimetext.com/) editor
* Sublime Text [**package manager**](https://packagecontrol.io/) with some packages installed by default such as:
    * [Sublimerge](http://www.sublimerge.com/)
    * [Markdown Preview](https://github.com/revolunet/sublimetext-markdown-preview)
    * [BracketHighlighter](https://github.com/facelessuser/BracketHighlighter)

## Download

1. Go to either [Github releases](https://github.com/Mortadelegle/Commander/releases) or [Bitbucket releases](https://bitbucket.org/Mortadelegle/commander/downloads)
2. Download the exe and execute it (It is an auto-extractable 7zip file)
3. Execute `cmder.exe`
4. Perform **First Time Setup**
5. Carry around as much as you want!

## First Time Setup

1. Write `git n YourName`
2. Write `git e YourEmail@mail.com`

This is the equivalent to do

1. Go to `\Cmder\vendor\msysgit\etc`
2. Change at least the `[user]` fields to yours

![User Screenshot](http://i.imgur.com/E9yPjsP.png)

## Keyboard shortcuts

### Tab manipulation

* `Ctrl + t` : new tab dialog (maybe you want to open cmd as admin?)
* `Ctrl + w` : close tab
* `Ctrl + d` : close tab (if pressed on empty command)
* `Shift + alt + number` : fast new tab: `1` - CMD, `2` - Powershell `*`
* `Alt + enter`: Fullscreen

### Shell

* `Shift + Up` : Traverse up in directory structure (lovely feature!)
* `End, Home, Ctrl` : Traversing text with as usual on Windows
* `Ctrl + r` : History search
* `Shift + mouse` : Select and copy text from buffer

## Features

### Cmder Aliases
You can define simple aliases with command `alias name=command`

All aliases will be saved in `/config/aliases` file

An example is the alias `subl` which will open SublimeText on the side of the console like in the first screenshot

### Git Aliases
`git lg` and `git lg2` which are prettier git log options
![Git lg screenshot](http://i.imgur.com/QOcvbeH.png)

### SSH Agent

To start SSH agent simply call `agent`, which is in the `bin` folder.

If you want to run SSH agent on startup, uncomment the line in `/vendor/init.bat`so it says `@call "%CMDER_ROOT%/bin/agent.cmd"`.

### Python Interpreter
You can call the Python Interpreter by typing `python`
If you do not provide arguments it will launch the python window on the side
But if you pass a `.py` file it will execute on a similar console.

## Roadmap

### MinGW vs MSYS

The use of `MinGW` instead of `MSYS` would mean we could take advantage of things such as GCC, but that may carry the split of Commander into a Light and a Heavy version

### Ruby

It has been suggested that way add some interpreted languages such as Ruby, and since it seems to weight <50 mb it is very possible it joins our project

### GPG/SSH

Although we tried integrating since day one, because the GPG git comes with makes it kinda difficult to look outside the predetermined folder, and changing the registry is kinda losing the portability (And our no modifications on the host philosophy)
Nevertheless, we will still try to make it.

## Additional Credits

Thanks to all these people, and many more I'm sure I am forgetting

### Cmder and Sublime Text integration initial idea

[Source](http://laravel.io/forum/02-24-2014-a-neat-way-integrate-cmder-and-sublime-text-seamlessly)
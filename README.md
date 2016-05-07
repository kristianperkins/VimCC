# VimCC
## About this branch
This branch is a test to repurpose the VimCC codebase into a version of the 
program 'less'. This didn't work as intended.

This branch will live on here for a bit longer, but will probably one day die.

## Regular VimCC README

**By default `tab` is binded to exit insert mode, this can be rebound in the vimrc!**

Dissatisfied with the existing editor in ComputerCraft (seriously, try using it 
while relying on alt-gr for special characters!) so I decided to port Vim.

This is far from a perfect port, but it gets the job done for quick code edits
on the fly. But I would still recommend opening the code files in a more well
built editor for longer editing. 

## Modes
The program comes with two mode, the primary 'vim' mode that works as closely
to the really deal as possibly. There is also a 'less' mode, which is a much
worse recreation, but it's there if you want it.

Note that the less mode still is a bit to close to the vim mode, so `:q` is
still needed to quit it, and the file can still be edited. Proceed with
caution.

## Forks
A fork of this program for the "OpenComputers" mod is available 
[here](https://github.com/Vexatos/VimOC). This is an "official" port, but I'm
not personally responsible for its development.

## Installation
There are two ways to install the program:
### Via the Installer
The installer is both available as part of this [repo](./installer),
and as a download from pastebin, which can be directly gotten in the game by
running the following command in a ComputerCraft terminal: 

	pastebin run j1NxmAzb

### Manually
download all the files from here.
All files needed for running are in the [vimfiles](./vimfiles) directory.

In ComputerCraft the files need to be placed as following:
	/utils/vimfiles/*

Then I would also recommend creating a `/bin` directory and copying the `vim`
file there, and then adding that directory to your path, to allowing for
starting vim anywhere without having all the other files clutter up your path.

### Updating
Delete the old files and download the new version.

## Features and Bugs
Most basic vim movements are here, along with some other features (deletion,
merging lines...)

### Feature availability
If the feature isn't listed below as not available then it probably is available,
or I might just not be aware of it.

### Vimrc
There are currently only very limited vimrc support. The default vimrc (with
usage information) is avalible [here](./vimfiles/vimrcDefault). A user
configured file can be placed in the ComputerCraft computers root directory, and
must be named `.vimrc`.

### Logging
There are logs, created in the hidden directory `.vimlog` in the ComputerCraft
computers root directory. By default the log level is set to `NONE`, but this
can be changed in the vimrc file.

Currently almost nothing is logged, but the support is there.
.
### Unsupported Features
- Ex commands!
- `~` (switch case)
- buffers (at least one)
- undo
- reverse find (`F` & `T`) 
- `.` (repeat last command)
- support for commands executed by holding down `CTRL` and another key
- Replace mode
- splits (like the screen is big enough for that...)
- syntax highlighting (but this shouldn't be to hard)
- better vimrc support
- `;` & `,`
- `(`, `)`, `{`, `}`, `[[`, `[]`, `]]`, `][`
- searching
- `%` (go to matching bracket)
- Line numbering
- Characters that aren't ASCII 7 (limitiation in ComputerCraft/Minecraft)
- useful user configuration

## Improving
If you are interested in trying to add new features or fix the already existing
ones, look to the [command](./vimfiles/command) since there is where both the vi
and the ex commands are defined.


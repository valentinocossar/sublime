## sublime

Plugin for Sublime Text, a cross platform text and code editor, available for Linux, Mac OS X, and Windows.

### Requirements

 * [Sublime Text](http://www.sublimetext.com/)


### Installation

#### Manual

1. Clone this repository somewhere on your machine. This guide will assume `~/.zsh/sublime`.

  ```sh
  git clone https://github.com/valentinocossar/sublime.git ~/.zsh/sublime
  ```

2. Add the following to your `.zshrc`:

  ```sh
  source ~/.zsh/sublime/sublime.plugin.zsh
  ```

3. Start a new terminal session.

#### Oh My Zsh

1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

  ```sh
  git clone https://github.com/valentinocossar/sublime.git $ZSH_CUSTOM/plugins/sublime
  ```

2. Add the plugin to the list of plugins for Oh My Zsh to load:

  ```sh
  plugins=(sublime)
  ```

3. Start a new terminal session.


### Usage

 * If `st` command is called without an argument, launch Sublime Text.

 * If `st` is passed a directory, `cd` to it and open it in Sublime Text (in the current window, if there is one open).

 * If `st` is passed a file, open it in Sublime Text (in the current window, if there is one open).

 * If `stt` command is called, it is equivalent to `st .`, opening the current folder in Sublime Text (in the current window, if there is one open).

 * If `sst` command is called, it is like `sudo st`, opening the file or folder in Sublime Text (in the current window, if there is one open). Useful for editing system protected files.

 * If `stp` command is called, it find a `.sublime-project` file by traversing up the directory structure. If there is no `.sublime-project` file, but if the current folder is a Git repo, opens up the root directory of the repo. If the current folder is not a Git repo, then opens up the current directory.

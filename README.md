# dotfiles | MacOS

## Installation

Linking:

```
ln -s ./dotfiles/.zshrc .zshrc
ln -s ./dotfiles/Preferences.sublime-settings ~/Library/Application Support/Sublime Text 3/Packages/User/Preferences.sublime-settings
ln -s ./dotfiles/pure.zsh /usr/local/lib/node_modules/pure-prompt/pure.zsh
```

Changing icons:

* Tutorial - http://hashbangstar.net/blog/changing-icons-in-el-capitan
* http://macreplacementicons.com/#mac_replacement_icons
* https://glaciericons.com/

### Terminal

Installing pure:

```
$ npm install --global pure-prompt
```

Changing the pre-prompt in pure.zsh to only give the currect directory rather than the entire path:
http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html

```
preprompt_parts+=('%F{blue}%1d%f')
```

### Sublime
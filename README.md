# dotfiles | MacOS

## Installation

Linking:

```
ln -s ./dotfiles/.zshrc .zshrc
ln -s ./dotfiles/Preferences.sublime-settings ~/Library/Application Support/Sublime Text 3/Packages/User/Preferences.sublime-settings
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

Changing the pre-prompt in pure:

```python
# Set the path.
# preprompt_parts+=('%F{blue}%~%f')
# New prompt set by me
preprompt_parts+=('%F{blue}%1d%f')
```

### Sublime
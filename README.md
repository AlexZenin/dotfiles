# dotfiles | MacOS

### Shell 

We want to ensure that the default bash shell is used. Catalina comes with `zsh` as the default terminal, but in case it's using something other than `zsh` or `bash`, run the following command to at least change it to bash:

```shell script
chsh -s /bin/bash
```

Remember to restart the terminal for the changes to take place.

#### Other commands

```bash
# Confirm what shell you are running
$ echo $0
# See what other shells are available
$ cat /etc/shells
```

### Homebrew

From wikipedia **_"Homebrew is a free and open-source software package management system that simplifies the installation of software on Apple's macOS and linux."_** 

[https://brew.sh/](https://brew.sh/)

```shell script
# Install homebrew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Install brew packages and casks

```shell script
brew bundle
```

### Docker

Open up the docker GUI application and run the following to test the installation

```shell script
docker run hello-world
``` 

### Node

```shell script
# First we want to install nvm (if you open up your bash profile after this has finished you will see some lines have been added)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash

# Ensure that nvm was correctly installed (you will need to close your shell and reopen it)
nvm --version

# Install the Long Term Support version of Node
nvm install --lts

# Check that node works
node -v

```
### Git
Setup SSH keys to clone repos through ssh 

```shell script
# This will generate your ssh keys and store them in your ~/.ssh/ directory
# Alternatively just run `ssh-keygen` and enter through all the options
ssh-keygen -P '' -f ~/.ssh/id_rsa

# This will copy your public key. 
cat ~/.ssh/id_rsa.pub | pbcopy

# Paste the keys in gitlab and github
```

Finally setup your username and email details as follows substituting Mona Lisa for your name and email.
```shell script
git config --global user.name "Mona Lisa"
git config --global user.email "Mona.Lisa@gmail.com"
```

### Oh-my-zsh

_Only run if zsh, curl and git are all installed and working_

```shell script
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Terminal

Installing pure:

```
$ brew install pure
```

Changing the pre-prompt in pure.zsh to only give the currect directory rather than the entire path:
http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html

```bash
# /usr/local/lib/node_modules/pure-prompt/pure.zsh
preprompt_parts+=('%F{blue}%1d%f')
```
### Powerline fonts

```shell script
# clone
git clone https://github.com/powerline/fonts.git --depth=1
# install
cd fonts
./install.sh
# clean-up a bit
cd ..
rm -rf fonts
```

### Defaults

```bash
defaults write -g InitialKeyRepeat -int 15 # Normal minimum
defaults write -g KeyRepeat -int 1 # Normal minimum is 2 (30ms)
defaults write -g com.apple.trackpad.scaling -float 2.5 # Not sure if this actually works
defaults write -g ApplePressAndHoldEnabled -bool false # For vim plugins
# Or if you want the behavious just on vscode
defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false
```

* Allow tabbing through dialogue boxes
* Allow button press with touchpad touch rather than click
* Minimise windows into application icon
* Trackpad speed - 1 off the fastest
* Hide the menu bar
* Show battery percentage
* Key hold allows key repeat
* Show password immediately
* Map the caps lock key to escape
* Keyboard -> text - remove text replacements
* Screen sleep time to 30min

### VSCode

Install Settings sync and sync settings through the settings sync plugin

### Chrome 

#### Plugins

**Regular Profile**
* Lastpass
* Vimium
* AdBlocker
* HTTPS Everywhere 
* Markdown
* Full Page Screenshot
* Redux Devtools

**Dev Profile**
* Blank New Tab
* Wappalyzer
* Proxy

#### Settings

* Downloads should go straight to desktop
## Linking Files (Optional)

```
ln -s ./dotfiles/.zshrc .zshrc
ln -s ./dotfiles/Preferences.sublime-settings ~/Library/Application Support/Sublime Text 3/Packages/User/Preferences.sublime-settings
```

### Icons

* Tutorial - http://hashbangstar.net/blog/changing-icons-in-el-capitan
* http://macreplacementicons.com/#mac_replacement_icons
* https://glaciericons.com/
# dotfiles

## Install softwares
* Debian/Ubuntu
```
sudo apt-get install -y ack-grep aria2 cmake ctags curl g++ gcc git tmux vim wget zsh
```

* Mac OS X
```
brew install vim
brew install zsh
```
## Config files

#### zsh
```
# Install prezto
zsh
git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done
chsh -s /bin/zsh
```

#### vim
```
bash <(curl -fsSL https://raw.githubusercontent.com/fabioperez/dotfiles/master/dottools/vimstall.sh)
```

#### tmux
```
wget -q https://raw.githubusercontent.com/fabioperez/dotfiles/master/.tmux.conf -O ~/.tmux.conf
```

## Tweaks

#### Ubuntu 14.04

##### Caps Lock as Control
Add the following line to `/etc/default/keyboard`:

```
XKBOPTIONS=“ctrl:nocaps”
```

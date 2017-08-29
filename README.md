# Dotfiles
My dotfiles (configuration files) for commonly used applications.

## Install dependencies and prep system

### Dev tools
- Download and install latest version of Xcode from the Mac App Store.
- Download and install Xcode Command Line Tools from https://developer.apple.com/downloads/.
- `brew install zsh zsh-completions` Install zsh
- `chsh -s $(which zsh)` Make zsh default shell
- `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` Install ohmyzsh

### nvim and zshell in iterm2

![Terminal and Vim](https://user-images.githubusercontent.com/896475/29837734-03967d6a-8cc7-11e7-839c-f69fcdaabe67.png)

## On MacOS
```
$ git clone https://github.com/pmarsceill/dotfiles ~/.dotfiles
```

Install GNU stow (optional)
```
$ brew install stow
```

Use Stow to create symlinks for each directory to `$HOME` (or do it yourself manually)
```
$ cd ~/.dotfiles
$ stow -t "$HOME" "bash"
$ stow -t "$HOME" "git"
$ stow -t "$HOME" "irc"
$ stow -t "$HOME" "git"
$ stow -t "$HOME" "iterm"
$ stow -t "$HOME" "vim"
$ stow -t "$HOME" "zsh"
```

## To do
- [ ] Automatically symlink all the directories with one command
- [ ] Add a setup script that installs application dependencies (like `brew install hub`, etc...)

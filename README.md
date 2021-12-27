# 42 Tips and Tricks

## 42 Tools
[Moulinette](https://moulinette.42lausanne.ch/)
[42evaluators](https://42evaluatiors.com)
[42url](https://42url.com/)

## Vim
### ⌨️ Shortcuts
- `ctrl + z` get back to shell
- `fg` get back to vim
- `i` insert mode
- `v` visual mode
- `ctrl + esc :w` save
- `ctrl + esc :x` save and quit
- `ctrl + esc :q` quit without saving
- `ctrl + esc :!q` force quit
- `yy then p` copy/past
- `dd` delete line
- `dw` delete word
- `x` delete char
- `r` replace char
- `:%s/foo/bar/g` search and replace

### 🔧 Configuration
- `:set number` show line number
- `:syntax on` turn on syntax highlighting
- `:set ruler` show numbers of columns
- `:set mouse -=a` allow copy/past mouse

# Git
#### configure gitignore as global
git config --global core.excludesfile ~/.gitignore_global

#### See changes of files modified
- `git diff` see changes of files modified

git clone --recurse-submodules

or if you have already cloned

git submodule init 
git submodule update

TLDR

In summary, if you want to contribute to a project, the simplest way is to:

    Find a project you want to contribute to
    Fork it
    Clone it to your local system
    Make a new branch
    Make your changes
    Push it back to your repo
    Click the Compare & pull request button
    Click Create pull request to open a new pull request

# GCC
#### Detect memory leaks
gcc -g3 -fsanitize=address

# Tarball
tar -cvf test.tar **/main.c
tar -xvf test.tar


# display ascii table
man ascii

### space used
du -sh *



https://recruitin.net/

alias ftsave="cd ~/42 && git add . && git commit -m \"autosave from home at `date +'%Y-%m-%d %H:%M:%S'`\" && git push"
alias ftsave="cd ~/42 && git add . && git commit -m \"autosave from 42 at `date +'%Y-%m-%d %H:%M:%S'`\" && git push"


https://emojipedia.org/direct-hit/
https://shields.io/
https://simpleicons.org/
https://tinypng.com/
https://www.base64-image.de/




# 42 Tips and Tricks

## 42 Tools
- [Moulinette](https://moulinette.42lausanne.ch/)
- [42evaluators](https://42evaluatiors.com)
- [42url](https://42url.com/)

## Vim
### ⌨️ Shortcuts
- `Ctrl + Z` Get back to shell
- `fg` Get back to vim
- `i` Insert mode
- `v` Visual mode
- `Ctrl + Esc :w` Save
- `Ctrl + Esc :x` Save and quit
- `Ctrl + Esc :q` Quit without saving
- `Ctrl + Esc :!q` Force quit
- `yy` Copy
- `p` Past
- `dd` Delete line
- `dw` Delete word
- `x` Delete char
- `r` Replace char
- `:%s/foo/bar/g` Search and replace

### 🔧 Configuration
- `:set number` Show line number
- `:syntax on` Turn on syntax highlighting
- `:set ruler` Show numbers of columns
- `:set mouse -=a` Allow mouse copy/past

## Git
### Configure gitignore as global
```
git config --global core.excludesfile ~/.gitignore_global
```
### See changes of files modified
```
git diff
```
### Clone repo with submodules
```
# first clone
git clone --recurse-submodules

# with repo already cloned
git submodule init 
git submodule update
```

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

## Detect memory leaks with GCC
```
gcc -g3 -fsanitize=address
```
## Debugging with LLDB
1. Run debugger 
```
lldb ./your-prog
```
2. Set breakpoint
```
breakpoint set --name ft_strlen
or
b ft_strlen
```
##### Sources
[debugging-with-lldb](https://kevinushey.github.io/blog/2015/04/13/debugging-with-lldb/)


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




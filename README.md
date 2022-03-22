# 42 Tips and Tricks

## Useful Links
- [Moulinette](https://moulinette.42lausanne.ch/)
- [42evaluators](https://42evaluatiors.com) - 42evaluators is originialy created to find an active student to set up a correction
- [42url](https://42url.com/) - U42url.com is a fast and free url shortener
- [42api](https://api.intra.42.fr/apidoc) - The 42 API provide programmatic access to read and write 42's data
- [42stud](https://www.https://www.42stud.com/.com/) - A minimal, clean, and student driven list of usefull 
- [42tools](https://github.com/solareenlo/42tools) - Collection of 42 tools

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

# already cloned
git submodule init 
git submodule update
```
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


## TLDR

In summary, if you want to contribute to a project, the simplest way is to:

    Find a project you want to contribute to
    Fork it
    Clone it to your local system
    Make a new branch
    Make your changes
    Push it back to your repo
    Click the Compare & pull request button
    Click Create pull request to open a new pull request





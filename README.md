# 42 Tips and Tricks

## Useful Links
- [Moulinette](https://moulinette.42lausanne.ch/) - Moulinette web interface
- [42evaluators](https://42evaluatiors.com) - 42evaluators is originialy created to find an active student to set up a correction
- [42url](https://42url.com/) - U42url.com is a fast and free url shortener
- [42api](https://api.intra.42.fr/apidoc) - The 42 API provide programmatic access to read and write 42's data
- [42stud](https://www.https://www.42stud.com/.com/) - A minimal, clean, and student driven list of usefull 
- [42tools](https://github.com/solareenlo/42tools) - Collection of 42 tools
- [recruitin](https://recruitin.net/) - Easily use Google to search profiles on LinkedIn

## ASCII
```
man ascii
```

## Vim
### Shortcuts
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

### Configuration
- `:set number` Show line number
- `:syntax on` Turn on syntax highlighting
- `:set ruler` Show numbers of columns
- `:set mouse -=a` Allow mouse copy/past

## Generate an SSH Key Pair
1. Open new terminal and type
```
cd ~/
```
2. Create an RSA key
```
ssh-keygen -b 2048 -t rsa
```
3. Complete fiedls.
4. Copy content of `id_rsa.pub`
```
cat ~/.ssh/id_rsa.pub
```
5. Go to [profile.intra.42.fr](https://profile.intra.42.fr/gitlab_users)
6. Add your public key

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
### Undo last git commit
```
git reset --soft HEAD~1
```
[more](https://devconnected.com/how-to-undo-last-git-commit/)

### Stashing and Cleaning
```
git stash
git stash pop
```
[more](https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning)

### Tagging
```
git tag -a v1.4 -m "my version 1.4"
git tag
git push --tags <repo-name>
```
[more](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
[more](https://stackabuse.com/git-push-tags-to-a-remote-repo/)

## Detect memory leaks
### GCC
```
gcc -g3 -fsanitize=address
```
### Valgrind
1. Install
```
sudo apt install valgrind  # Ubuntu, Debian, etc.
sudo yum install valgrind  # RHEL, CentOS, Fedora, etc.
sudo pacman -Syu valgrind  # Arch, Manjaro, Garuda, etc
```
2. Usage
```
valgrind --leak-check=full \
         --show-leak-kinds=all \
         --track-origins=yes \
         --verbose \
         --log-file=valgrind-out.txt \
         ./executable exampleParam1
```
## Debugging
### LLDB
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
### VS Code
[source](https://code.visualstudio.com/docs/editor/debugging)

## References
- [kevinushey](https://kevinushey.github.io/blog/2015/04/13/debugging-with-lldb/) - Debugging with lldb
- [stackoverflow](https://stackoverflow.com/questions/5134891/how-do-i-use-valgrind-to-find-memory-leaks) - How to Run Valgrind

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





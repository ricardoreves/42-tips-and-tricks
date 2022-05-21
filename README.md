# 42 Tips and Tricks

## Useful Links
- [moulinette](https://moulinette.42lausanne.ch/) - Moulinette web interface
- [42evaluators](https://42evaluators.com/) - 42evaluators is originialy created to find an active student to set up a correction
- [42url](https://42url.com/) - U42url.com is a fast and free url shortener
- [42api](https://api.intra.42.fr/apidoc) - The 42 API provide programmatic access to read and write 42's data
- [42stud](https://www.https://www.42stud.com/.com/) - A minimal, clean, and student driven list of usefull 
- [42tools](https://github.com/solareenlo/42tools) - Collection of 42 tools
- [recruitin](https://recruitin.net/) - Easily use Google to search profiles on LinkedIn
- [onlinegdb](https://www.onlinegdb.com/online_c_compiler) - Online compiler and debugger for c/c++
- [stacked-crooked](http://coliru.stacked-crooked.com/) - Online compiler for c/c++
- [robozzle.com](http://robozzle.com/js/index.aspx) - Robozzle is a robot-programming game

## ASCII
```
man ascii
```

## SHELL
- [explainshell.com](https://explainshell.com/explain?cmd=grep.1%20-oE%20%22ERROR%7CWARN%22%20%2Alog%2A%20%7C%20sort%20%7C%20uniq%20-cDFLAGS
) - Write down a command-line to see the help text that matches each argument
- [command-not-found.com](https://command-not-found.com/) -  Install any command on any operating system. 

### 42 Homebrew
1. Install Homebrew properly on your 42 session
```
curl -fsSL https://rawgit.com/kube/42homebrew/master/install.sh | zsh
```
2. [Learn more](https://github.com/kube/42homebrew)

## Find and Launch Mac Apps
- `Command (⌘) + Space`

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
4. Copy content of the public key
```
cat ~/.ssh/id_rsa.pub
```
5. Go to [profile.intra.42.fr](https://profile.intra.42.fr/gitlab_users)
6. Add the copied public key

## Git
### Authentification
- [source](https://docs.github.com/en/authentication)

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
- [source](https://devconnected.com/how-to-undo-last-git-commit/)

### Stashing and Cleaning
```
git stash
git stash pop
```
- [source](https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning)

### Tagging
```
git tag -a v1.4 -m "my version 1.4"
git tag
git push --tags <repo-name>
```
- [source](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
- [source](https://stackabuse.com/git-push-tags-to-a-remote-repo/)

### Delete branch
```
# delete remote branch
git push -d origin <branch_name>

# delete local branch
git branch -d <branch_name>
```

### Change a Git remote URL
```
git remote set-url origin <git@github.com:username/project.git>
```

## VSCODE Debug
- [gourav.io](https://gourav.io/blog/setup-vscode-to-run-debug-c-cpp-code) - 

## Detect memory leaks
### GCC
```
gcc -g3 -fsanitize=address
```

### Diff
On Unix-like operating systems, the diff command analyzes two files and prints the lines that are different. In essence, it outputs a set of instructions for how to change one file to make it identical to the second file.
```
diff -u file1.txt file2.txt
```
- [source](https://www.computerhope.com/unix/udiff.htm)

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
1. Launch lldb `lldb <prog> <arg1> <arg2>`
2. Set breakpoint `b <funct_name>`
3. Launch the executable in the debugger `run`
4. Some helpful commands
```
  expression      -- Evaluate an expression on the current thread.  Displays
                       any returned value with LLDB's default formatting.
  frame           -- Commands for selecting and examing the current thread's
  gui             -- Switch into the curses based GUI mode.
  help            -- Show a list of all debugger commands, or give details
                       about a specific command.
  target          -- Commands for operating on debugger targets.
  
  b         -- Set a breakpoint using one of several shorthand formats.
  bt        -- Show the current thread's call stack.  Any numeric argument
               displays at most that many frames.  The argument 'all' displays
               all threads.  Use 'settings set frame-format' to customize the
               printing of individual frames and 'settings set thread-format'
               to customize the thread header.
  c         -- Continue execution of all threads in the current process.
  display   -- Evaluate an expression at every stop (see 'help target
               stop-hook'.)
  j         -- Set the program counter to a new address.
  kill      -- Terminate the current target process.
  l         -- List relevant source code using one of several shorthand formats.
  n         -- Source level single step, stepping over calls.  Defaults to
  p         -- Evaluate an expression on the current thread.  Displays any
               returned value with LLDB's default formatting.
  q         -- Quit the LLDB debugger.
  r         -- Launch the executable in the debugger.
  s         -- Source level single step, stepping into calls.  Defaults to
  v         -- Show variables for the current stack frame. Defaults to all
               arguments and local variables in scope. Names of argument,
               local, file static and file global variables can be specified.
               Children of aggregate variables can be specified such as
               'var->child.x'.  The -> and [] operators in 'frame variable' do
               not invoke operator overloads if they exist, but directly access
               the specified element.  If you want to trigger operator
               overloads use the expression command to print the variable
               instead.
               It is worth noting that except for overloaded operators, when
               printing local variables 'expr local_var' and 'frame var
               local_var' produce the same results.  However, 'frame variable'
               is more efficient, since it uses debug information and memory
               reads directly, rather than parsing and evaluating an
               expression, which may even involve JITing and running code in
               the target program.

```
- [Learn the lldb debugger basics in 11 minutes](https://www.youtube.com/watch?v=v_C1cvo1biI)
- [GDB to LLDB command map](https://lldb.llvm.org/use/map.html)

### VS Code
- [source](https://code.visualstudio.com/docs/editor/debugging)

## Screenshot
### Ubuntu
- `Print Screen` to take a screenshot of the desktop.
- `Alt + Print Screen` to take a screenshot of a window.
- `Shift + Print Screen` to take a screenshot of an area you select.
### MacOS
- `Shift + Command + 3` to take a screenshot of the desktop.
- `Shift + Command + 4` to take a screenshot of a portion of the screen
- `Shift + Command + 4 + Space` to take a screenshot of a window or menu
### Firefox
- `Ctrl + Shift + S` to take a screenshot of full page.

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
    
```
sudo apt  install universal-ctags
ctags -x -f - --c-kinds=f push_swap.c
ctags -x --c-kinds=fp push_swap.c | awk '{$1=$2=$3=$4=""; print $0}' | awk '{$1=$1};1' | sed -z 's/\n/;\n/g'
ctags -x --c-kinds=fp utils.c | awk '{$1=$2=$3=$4=""; print $0}' | awk '{$1=$1};1' | sed -z 's/\n/;\n/g'
```
 





% Introduction to bash
% SageDays FPSAC2019
# The file structure

Everything lives in `/`, the root of the file system.

Each file is reached by following a path in the tree.

![Unix File Structure](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Standard-unix-filesystem-hierarchy.svg/1024px-Standard-unix-filesystem-hierarchy.svg.png)

# Navigating the file structure

- Most of the file you need are in your home directory `/home/enadeau`.
- Navigate with the `cd` (*change directory*) command. Paths are relative to
  your position in the tree.
  - `../` goes up one level
  - Going  to in your papers folder `cd Documents/papers`
  - Going  to the root `cd /`
  - Going  to your home directory `cd` or `cd ~`
  - Going one level up in the tree `cd ..` or two levels `cd ../..`

- You're lost? `pwd` (*print working directory*) to see where you are.

# Navigating the file structure

- List all files in the current directory with `ls`

Filename that starts with a dot are hidden

- You can see them with `ll` or `ls -a`

- See the content of a file with `cat <file>`

# Modifying file

- remove file `rm <file>`
- copy file `cp myfile destination_folder`
- move and rename file `mv <current_name> <new_name>`
- make a directory `mkdir <name>`

The star acts as a joker `rm *.py` remove all python files in your current
directory.

# Search and find

- to search into a file use a grep command
```bash
grep tableua paper.tex
```
- to search for a file
```bash
find ~/ -name 'lost_code.py'
```

# Random useful thing you can do

- Starting a program ex: `sage` or `sage --notebook=jupyter`
- Stop the running program by hitting `ctrl-c`
- Complete the command you are writing by pressing `tab`
- creating shortcuts for things that you do a lot with *aliases* (*e.g.* sagen)
- pass results of a command to an other with the *pipe* mechanism
```bash
ls | grep .py
```
The results of `ls` is passed to `grep`

# Getting help on the command

- man page with `man mv`
- help (`--help`, `-h`) `mv --help`
- [tldr](https://github.com/tldr-pages/tldr) (needs to be installed) `tldr mv`
    - On Debian-based system `sudo apt install tldr`


# Going further

- [Software Carpentry](http://swcarpentry.github.io/shell-novice/)
- [Game Shell](http://lama.univ-savoie.fr/~hyvernat/Enseignement/1617/info202/tp2.html) (French only)

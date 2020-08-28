# Unix terminal

## Mac OS

- [Iterm 2](https://www.iterm2.com/downloads.html)

## ZSH

- [zsh](https://www.zsh.org/)
- [Oh My zsh](https://ohmyz.sh/)

## Fish Shell

- [Fishshell](https://fishshell.com/)

## Tools

- [ncdu - NCurse Disk Usage](https://dev.yorhel.nl/ncdu)
- [thefuck - Corrects errors in previous console commands](https://github.com/nvbn/thefuck)
- [multitail](https://www.vanheusden.com/multitail/)

## Commands

### Get number of files by types

```sh
# find . -type f : Get all files (Location "." )
# sed 's/.*\.//' : Get only the extension
# sort : sorting
# uniq -c : Get uniq with -c for the counter 
find . -type f | sed 's/.*\.//' | sort | uniq -c
# Result
#  19 scss
#   7 svg
#  91 ts
```

### Chmod +x on Windows

```sh
git update-index --chmod=+x myScript.sh
```

## Articles

- [iTerm 2 + fish + fisherman + Material Design + Meslo](https://gist.github.com/ghaiklor/5c393e1c27cab79a9258)

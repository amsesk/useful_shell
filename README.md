### Read a file into a zsh array, splitting on newline
```
IFS=$'\n'
array=($(cat /path/to/file))
```

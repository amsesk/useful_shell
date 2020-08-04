### Read a file into a zsh array, splitting on newline
```
IFS=$'\n'
array=($(cat /path/to/file))
```

### Read a file line by line, check if each line occurs in an array, print if it doesn't
```
while read p; do
if [[ ! ${arr[(ie)$p]} -le ${#arr} ]]; then
echo $p
fi
done < all.headers > part2.headers
```

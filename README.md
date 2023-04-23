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

### Add branch of forked remote to local copy of a git repositiory
```
git remote add <remote_name/username> https://github.com/username/repo.git
git remote -v
git fetch <remote_name/username>
git checkout -b <my_name_for_their_branch> <remote_name/username>/<their_branch_name>
```

### Set a device as manager/unmanaged with NetworkManager - useful when wanting to stop using Wifi connection
```
nmcli d #get device list
nmcli d set <device> managed no
nmcli d set <device> managed yes
```

# Linux And Bash For Data Engineering

## Week 4

### Searching The File System


### Locate command in Linux
```
sudo yum install mlocate
sudo updatedb
locate .zshrc
```

```
locate .ZSHRC
```

```
locate -i .ZSCRC
```

```
mkdir other
touch other/.zshrc
locate .zshrc
```

### Find command in Linux

```
find . -name .zshrc
```

```
sudo find / -name .zshrc
```

```
time sudo find / -name .zshrc
time locate .zshrc
```

### Using xargs

```
touch /tmp/foo{0..10}.txt
ls -l /tmp
```

```
find /tmp -name foo* -type f -print
```

```
mkdir /tmp/fooDIR
find /tmp -name foo* -type f -print | xargs /bin/rm -f
find /tmp -name foo* -type f -print
```

### Using mdfind in OSX

```
man mdfind
```

```
mdfind -name readme.txt -onlyin .
```

```
touch readme.txt
mdfind -name readme.txt -onlyin .
```

```
mdfind -name readme.txt -onlyin . -live
```

```
mdfind -name readme.txt -onlyin . date:12/1/2011-12/1/2021
```

```
mdfind 'KMDItemFSSize >= 10000000000'
```

```
mdfind 'KMDItemFSSize >= 10000000000' | xargs du -sh
```
```
mdfind 'KMDItemFSSize >= 10000000000' | grep Xcode | xargs du -sh
```

### Lab Task 1
```
find -name "*.csv"
```
```
 find -name "*.txt"
```
```
find -name "*.txt" | xargs grep Apple
```
```
grep -R Banana .
```

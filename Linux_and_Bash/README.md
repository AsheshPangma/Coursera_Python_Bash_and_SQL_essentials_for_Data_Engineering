# Linux And Bash For Data Engineering

## Week 4

### Searching The File System


#### Locate command in Linux
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

#### Find command in Linux

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

#### Using xargs

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

#### Using mdfind in OSX

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

#### Lab Task 1
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


### Modifying Files, Directories, Permission and Archiving

#### Moving Files and Directories in linux

```
mkdir -p bar/bam/biz
ls -l bar
ls -lR bar
```
```
touch bar/one.txt
touch bar/bam/two.txt
touch bar/bam/biz/three.txt
ls -lR bar
```

```
mv bar /tmp/
ls
cd /tmp
ls
```
```
cp -r bar/bam .
ls
cd bam
ls
cd biz
ls
```

```
touch foo/two.txt
rsync -av foo/ newspot/foo/
```

#### Setting Permission on Files and Directories in Linux

```
chmod 777 script.sh
ls -l
chmod 4000 script.sh
ls -l
./script.sh
```
The `script.sh` script does not run as the permission is denied.

```
chmod +x script.sh
./script.sh
```
```
whoami
```

#### Archiving Data in Linux

To zip
```
zip -r archives/foo.zip foo
```
To unzip
```
unzip foo.zip
```

To archive using Tar
```
tar -zcvf archives/foo.tgz foo
```
To unarchive
```
tar -zxvf foo.tgz
```





#### Lab Task 2

```
chmod -R -x *.py
./one.py
```
```
chmod +x one.py
./one.py
```


### Processing Text










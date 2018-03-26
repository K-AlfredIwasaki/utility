### vim
- use a instead i

- move around
- move by one word
```
b or w 
```

- move to the beginning/end of the line
```
0 or $
```
 
- move to the beginning of the doc
```
gg
```

- move to the end of the doc
```
shift + ga
```

- delete
```
daw, caw, dd
```

- substitute
```
s
```

- jump to the line
```
vi +36 filename
or
:36

```

- copy and paste between terminals
```
"+yy
"+p
```
- copy and paste within a file
```
v, y or x, p
```
https://www.datacamp.com/community/tutorials/shell-commands-data-scientist

- find
```
The following searches the tree structure starting in the current directory (".") for any file starting with "iris" and ending in any dumber of characters ("-name 'iris*'") of regular file type ("-type f"):
```

```
find . -name 'iris*' -type f
```


### command line
append line to a file 
```
echo hello world >> my_file.txt
```

count the number of files in the directory
```
ls -l directory | wc -l
```

- Concatenate files with cat
```
cat file_1.csv file_2.csv > target_file.csv
```

- Modify a file with sed
```
sed "s/<string to replace>/<string to replace it with>/g" <source_file> > <target_file>.
```

```
sed "s/, ?,/,,/g" adult.csv >  adult.csv
```

- sort
columns separated by '|', sort on column 2 (-k2), case insensitive (-f)
The -n and -r parameters allow you to sort numerically and in reverse order, respectively

```
sort data.csv | uniq -c | sort -nr | head -n 7
```

- uniq
Sometimes you want to check for duplicate records in a large text file - that's when uniq comes in handy

```
sort data.csv | uniq -c | sort -nr | head -n 7
```


### iterm

- move between panes
```
cmd + [ or ]
```

- move between tabs
```
cmd + 1, 2, 3, 4,,,
```

- split 

```
cmd + d --- vertically
cmd + shift + d --- horizontally

```


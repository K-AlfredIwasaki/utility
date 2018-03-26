#vim
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
The following searches the tree structure starting in the current directory (".") for any file starting with "iris" and ending in any dumber of characters ("-name 'iris*'") of regular file type ("-type f"):

```
find . -name 'iris*' -type f
```


# command line
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







# iterm

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


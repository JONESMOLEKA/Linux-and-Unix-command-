Diff command in Linux is used to compare the content of two files line by line and if the difference is found then it will also list differences along with line numbers. Diff command can also be used to compare the contents of two directories.

**Syntax :**
```
diff [options] File1 File2 
```

**Special symbols are:**

Symbol |Meaning
-------|--------
A	|Add
C	|Change
D	|Delete
'#'	| Line numbers
'– – –'	|Separates Files in Output
<	|File 1
'>'	|File 2

Options	|Description
--------|-----------
 –normal	| The output displayed is a normal difference (the one that is displayed by default)
-q, –brief	|It reports only if the files differ
-s, –report-identical-files	 |It reports if two files are the same and have no differences between them
 -y, –side-by-side	|The output is displayed in two-column format
 -t, –expand-tabs	|It will help in expanding the tabs to spaces in the output format.
 -r, –recursive	|It will recursively help in comparing any subdirectories that are found
 -i, –ignore-case	|This option is used in ignoring any case diff in file data.
 -a, –text	 |This option will be treating all the files as text
 –help	 |Prints the options that are available and will exit
-v, –version	 |output version information and exit

**Examples** 

Lets say we have two files with names a.txt and b.txt containing 5 Indian states.

- $ ls
```
a.txt  b.txt
```

- $ cat a.txt
```
Gujarat
Uttar Pradesh
Kolkata
Bihar
Jammu and Kashmir
```

- $ cat b.txt
```
Tamil Nadu
Gujarat
Andhra Pradesh
Bihar
Uttar pradesh
```

Now, applying diff command without any option we get the following output:

- $ diff a.txt b.txt
```
0a1
> Tamil Nadu
2,3c3
< Uttar Pradesh
 Andhra Pradesh
5c5
 Uttar pradesh
```


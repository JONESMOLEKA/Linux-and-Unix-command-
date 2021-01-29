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


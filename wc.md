wc stands for word count. As the name implies, it is mainly used for counting purpose.

- It is used to find out number of lines, word count, byte and characters count in the files specified in the file arguments.
- By default it displays four-columnar output.
- First column shows number of lines present in a file specified, second column shows number of words present in the file, third column shows number of characters present in file and fourth column itself is the file name which are given as argument.

**Syntax**

`wc [OPTION]... [FILE]...`

options | Description 
--------|------------
wc -l | Prints the number of lines in a file.
wc -w | prints the number of words in a file.
wc -c | Displays the count of bytes in a file.
wc -m | prints the count of characters from a file.
wc -L | prints only the length of the longest line in a file.

**Examples** 
- wc test.txt
- wc -l test.txt ( gives number of line number of a file )
- wc -c test.txt
- wc -w 

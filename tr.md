- The tr command accepts input from standard input 
- This command takes two arguments which specify two character sets 
- The first character set is replaced by the equivalent member in the second character set 
- the -s option is used to squeeze several occurrences of a character to one character 

**Syntax**
```
tr [-Ccsu] string1 string2 
```

option | description 
-------|------------
-C	|Complement the set of characters in string1, that is "-C ab" includes every character except for 'a' and 'b'.
-c	|Same as -C but complement the set of values in string1.
-d	|Delete characters in string1 from the input.
-s	|Squeeze multiple occurrences of the characters listed in the last operand (either string1 or string2) in the input into a single instance of the character. This occurs after all deletion and translation is completed.
-u	|Guarantee that any output is unbuffered.


**Examples** 
-tr -cs "[:alpha:]" "\n" < file1
```
Create a list of the words in file1, one per line, where a word is taken to be a maximal string of letters.
```

- tr "[:lower:]" "[:upper:]" < file1
```
Translate the contents of file1 to uppercase.
```

- tr -cd "[:print:]" < file1
```
Remove all non-printable characters from file1.
```

- tr -s " " < file1
```
to remove all empty spaces 
```

The xargs command reads lines of text from the standard input or from the output of another command and turns them into commands and execute them.

You’ll often find xargs command being used with the find command. The find command gives you a list of filenames and the xargs command lets you use those filenames, one by one, as if it was input to the other command.

**syntax**
```
xargs [options] [command [initial-arguments]]
```

**Examples**
- $ find . -type f -name "*.txt" | xargs grep -l red
```
./three_lotus.txt
./two_lotus.txt
./rose.txt
```

**Dealing with file names with spaces**

If you have file with space in its name, it will cause issues. Let’s say I renamed three_lotus.txt to “three lotus.txt”. Now when it is processed via xargs, it is seen as two separate files as three and lotus.txt.

- find . -type f -name "*.txt" | xargs grep -l red
```
./two_lotus.txt
grep: ./three: No such file or directory
grep: lotus.txt: No such file or directory
./rose.txt
```
In such cases, you should use the -print0 option of the find command. It separates lines with ASCII null characters instead of newline characters. Similarly, you should also use xargs with -0 to accept the ASCII nulls.

- find . -type f -print0 -name "*.txt" | xargs -0 grep -l red
```
./two_lotus.txt
./three lotus.txt
./rose.txt
```
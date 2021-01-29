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

**See what command is being executed**

If you want to see what command is being executed with the help of xargs, you can use the -t option. It will print the actual command being executed.

- find . -type f -name "*.txt" | xargs -t touch
```
touch ./three_lotus.txt ./two_lotus.txt ./lily.txt ./rose.txt
```

**Force xargs to prompt for confirmation before running the command**

Some situations demand to be extra careful like deleting files. It will be a good idea to see what command is going to be executed and have the option to deny the execution.

You can use the -p option of xargs to get the prompt.

- find . -type f -name "*.txt" | xargs -p rm
```
rm ./three_lotus.txt ./two_lotus.txt ./lily.txt ./rose.txt ?...n
```

**Using placeholder with xargs to get more control over it**

By default, the xargs command adds the standard input as argument at the end of the command. This creates a problem when you need to use that before the last argument.

For example, if you use the move command, you need the source first and then the target. If you want to move the found files to a target directory, this command won’t work:

- find . -type f -name "*.txt" | xargs -p mv new_dir
```
mv new_dir ./three_lotus.txt ./two_lotus.txt ./lily.txt ./rose.txt ?...y
mv: target './rose.txt' is not a directory
```

This is where you can use placeholders in xargs with option -I like this:

- find . -type f -name "*.txt" | xargs -p -I {} mv {} new_dir
```
mv ./three_lotus.txt new_dir ?...n
mv ./two_lotus.txt new_dir ?...n
mv ./lily.txt new_dir ?...n
mv ./rose.txt new_dir ?...n
```

Think of it as if xargs gets all the file names from the find command and keep it in {}. Then it goes to the mv command and supplies the content of {}.

The major difference here is that instead of putting all the file names in the same command, it adds them one by one. This is why the mv command’s been called for each argument (as you can see in the above example).

**Note:** I used {} as placeholder. You could most other letters or characters as placeholder. {} is safe bet and easy to understand and distinguish.


**Running multiple commands with xargs**

You may use the placeholders to run multiple commands with xargs.

- find . -type f -name "*.txt" | xargs -I {} sh -c 'ls -l {}; du -h {}' 

```
-rw-rw-r-- 1 abhishek abhishek 0 May 28 17:02 ./three_lotus.txt
0	./three_lotus.txt
-rw-rw-r-- 1 abhishek abhishek 0 May 28 17:02 ./two_lotus.txt
0	./two_lotus.txt
-rw-rw-r-- 1 abhishek abhishek 0 May 28 17:02 ./lily.txt
0	./lily.txt
-rw-rw-r-- 1 abhishek abhishek 0 May 28 17:02 ./rose.txt
0	./rose.txt
```

**their is more .....**

docker ps -q | xargs docker stop

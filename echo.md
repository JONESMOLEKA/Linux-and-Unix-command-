echo command in linux is used to display line of text/string that are passed as an argument . This is a built in command that is mostly used in shell scripts and batch files to output status text to the screen or a file.

**Syntax :**
```
echo [option] [string]
```

**Options of echo command**

**NOTE :-** -e here enables the interpretation of backslash escapes

**1. \b :** it removes all the spaces in between the text

**Example :**
```
echo -e "Geeks \bfor \bGeeks"
```

**2. \n :** this option creates new line from where it is used.

**Example :**
```
 echo -e "Geeks \nfor \nGeeks"
```

**3. \t :** this option is used to create horizontal tab spaces.

**Example :**
```
echo -e "Geeks \tfor \tGeeks"
```

**4. echo * :** this command will print all files/folders, similar to ls command .
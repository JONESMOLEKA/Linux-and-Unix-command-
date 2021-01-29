the chmod command sets the permissions of files or directories.

**Syntax**
```
chmod [OPTION]... MODE[,MODE]... FILE...
chmod [OPTION]... OCTAL-MODE FILE...
chmod [OPTION]... --reference=RFILE FILE...
```

Options | Description 
--------|------------
-c, --changes |Like --verbose, but gives verbose output only when a change is actually made.
-f, --silent, --quiet | Quiet mode; suppress most error messages.
-v, --verbose | Verbose mode; output a diagnostic message for every file processed.
--no-preserve-root |Do not treat '/' (the root directory) in any special way, which is the default setting.
--preserve-root  | Do not operate recursively on '/'.
--reference=RFILE   | Set permissions to match those of file RFILE, ignoring any specified MODE.
-R, --recursive   | Change files and directories recursively.
--help   | Display a help message and exit.
--version   | Output version information and exit.

**Examples** 
- chmod 644 file.htm
```
Set the permissions of file.htm to "owner can read and write; group can read only; others can read only".
```

- chmod -R 755 myfiles
```
Recursively (-R) Change the permissions of the directory myfiles, and all folders and files it contains, to mode 755: User can read, write, and execute; group members and other users can read and execute, but cannot write.
```

- chmod u=rw example.jpg
```
Change the permissions for the owner of example.jpg so that the owner may read and write the file. Do not change the permissions for the group, or for others.
```
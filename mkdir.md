mkdir command in Linux allows the user to create directories (also referred to as folders in some operating systems ). This command can create multiple directories at once as well as set the permissions for the directories. It is important to note that the user executing this command must have enough permissions to create a directory in the parent directory, or he/she may recieve a ‘permission denied’ error.

**Syntax:**
```
mkdir [options...] [directories ...]
```

options | Description 
--------|------------
-m=mode,--mode=mode    | You can use the -m option to set a file mode (permissions, etc.) for the created directories. The syntax of mode is the same as with the chmod command.
-p,--parents	| Create parent directories as necessary. When this option is specified, no error is reported if a directory already exists.
-v,--verbose	| Verbose output. Print a message for each created directory.
-Z=context,--context=context|	If you are using SELinux, this option sets the security context of each created directory to context. For detailed information about security contexts, consult your SELinux documentation.
--help	|Display a help message, and exit.
--version	|Display version information, and exit.

**Example**
- mkdir -p /home/hope/Documents/pdf
- mkdir dest
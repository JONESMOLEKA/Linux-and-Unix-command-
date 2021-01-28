the pwd command outputs the name of the working directory.

**Syntax**

`pwd [OPTION]...`

**options**

Options | Description
------------|------------
-L,--logical	|If the environment variable PWD contains an absolute name of the current directory with no "." or ".." components, then output those contents, even if they contain symbolic links. Otherwise, fall back to default (-P) behavior.
-P,--physical	|Print a fully resolved name for the current directory, in which all components of the name are actual directory names, and not symbolic links.
--help	|Display a help message, and exit.
--version	|Display version information, and exit.
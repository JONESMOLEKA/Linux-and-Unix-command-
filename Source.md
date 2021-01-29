- The source command can be used to load any functions file into the current shell script or a command prompt.
- It read and execute commands from given FILENAME and return.
- The pathnames in $PATH are used to find the directory containing FILENAME. If any ARGUMENTS are supplied, they become the positional parameters when FILENAME is executed.

In other words The source command is a handy utility that can be used to refresh environment variables.


**Syntax**

```
source filename [arguments]
source functions.sh
source /path/to/functions.sh arg1 arg2
source functions.sh WWWROOT=/apache.jail PHPROOT=/fastcgi.php_jail
```
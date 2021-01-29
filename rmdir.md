rmdir command is used remove empty directories from the filesystem in Linux. The rmdir command removes each and every directory specified in the command line only if these directories are empty. So if the specified directory has some directories or files in it then this cannot be removed by rmdir command.

**syntax**

```
rmdir [-p] [-v | –verbose] [–ignore-fail-on-non-empty] directories …
```
options | Description 
--------|------------
–help | It will print the general syntax of the command along with the various options that can be used with the rmdir command as well as give a brief description about each option.
rmdir -p | In this option each of the directory argument is treated as a pathname of which all components will be removed, if they are already empty, starting from the last component.
rmdir -v, –verbose| This option displays verbose information for every directory being processed.
rmdir –ignore-fail-on-non-empty | This option do not report a failure which occurs solely because a directory is non-empty. Normally, when rmdir is being instructed to remove a non-empty directory, it simply reports an error. This option consists of all those error messages.
rmdir –version | This option is used to display the version information and exit.
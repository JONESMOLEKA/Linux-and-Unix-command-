cp command copies a file or group of files

**syntax** 

`cp [options] source dest`

Option	| Description according to GNU utils
--------|------------------------------------
-a	|Preserve as much as possible of the structure and attributes of the original files in the copy
-d	|Copy symbolic links as symbolic links rather than copying the files that they point to, and preserve hard links between source files in the copies.
-f or –force	|This option forces the copy even if the destination folder is not available for writing.
-i or –interactive	|Displays a message each time a file is to be overwritten.
-l	|Make hard links instead of copies of non-directories.
-R or -r or –recursive	|Copy directories recursively. By default, do not follow symbolic links in the source.
-s or –symbolic-link	|In this case, the command will make symbolic links of all files that are not folders. This replaces a copy.
-u or –update	|This option does not copy files that have the same or newer modification timestamp in the destination folder. It is an update of a copy.
-v or –verbose	|Print the name of each file before copying it.
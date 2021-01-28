the cd command ("change directory") changes the shell's current working directory.

cd is among the commands you use most often on the command line. It changes your working directory. Use it to move around in the hierarchy of your file system.

**Syntax**
`cd [-L | -P [-e]] directory`

Options| Description
-------|------------
-L	|Force symbolic links to be followed. In other words, if you tell cd to move into a "directory", which is actually a symbolic link to a directory, it moves into the directory the symbolic link points to. This option is the default behavior of cd; normally, it will always act as if -L was specified.
-P	|Use the physical directory structure without following symbolic links. In other words, only change into the specified directory if it actually exists as named; symbolic links are not followed. This option is the opposite of the -L option, and if they are both specified, this option is ignored.
-e	|If the -P option is specified, and the current working directory cannot be determined, this option tells cd to exit with an error. If -P is not specified along with this option, this option has no function.

**The root directory**
The root directory is the first directory in your filesystem hierarchy. All other directories are subdirectories of the root directory.

The root directory is represented by a single slash ("/").

To change into the root directory, making it your working directory, use the command:

`cd /`

**The working directory**
The current directory, regardless of which directory it is, is represented by a single dot (".").

So, running this command:

`cd .`

...would change us into the current directory. In other words, it would do nothing.

What's actually happening is the dot represents the "assumed" directory; it's a placeholder, and you can use the dot anywhere in a directory name. So, the command:

`cd documents`
...is the same as the command:

`cd ./documents`
...and also the same as:

`cd documents/.`
...as well as:

`cd ./documents/.`
In all of these examples, the dot represents "the directory assumed to be there". You can use it as a placeholder anywhere you want to tell the shell that a directory goes in that place, and to assume the appropriate value.
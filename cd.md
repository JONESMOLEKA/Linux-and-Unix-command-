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

**The parent directory**

The parent directory of the current directory — in other words, the directory one level up from the current directory, which contains the directory we're in now — is represented by two dots ("..").

So, If we were in the directory /home/username/documents, and we executed the command:

`cd ..`

...we would be placed in the directory /home/username.

The double-dot ("..") directory notation can be used anywhere in a directory name to represent going up one level. For instance, if we have two directories, /home/username/documents and /home/username/downloads, and we are currently in /home/username/documents, we could type the following:

`cd ../downloads`

...and we would be placed in /home/username/downloads.

**Your home directory**

Your home directory is the directory you're placed in, by default, when you open a new terminal session. It's the directory that holds all your settings, your mail, your default documents and downloads folder, and other personal items. It has a special representation: a tilde ("~").

So, if our username is username, and our home directory is /home/username, the command:

`cd ~`

...is functionally the same as the command:

`cd /home/username`

...and we can always access the subdirectories of our home directory by placing the tilde as the first component of the directory name. For instance, if your documents folder is named /home/username/documents, you can always move into that directory using the command:

`cd ~/documents`

**The previous working directory**

After you change directory, you can change back to the previous working directory by representing it with a dash ("-"). When you do this, the shell automatically tells you the new directory name.

`cd -`
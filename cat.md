The cat command reads one or more files and prints their contents to standard output. Files are read and output in the order they appear in the command arguments.

**Syntax**

`cat [options] [files]`

Option|	Description
------|-------------
-b	|Starting at 1, number non-blank output lines.
-e	|Display control and non-printing characters followed by a $ symbol at the end of each line. (May require the -v option)
-n	|Starting at 1, number all output lines.
-t	|Each tab will display as ^I and each form feed will display as ^L. (May require the -v option)
-u	|Output is displayed unbuffered.
-v	|Display control and non-printing characters. Control characters print as ^B for control-B. Non-ASCII characters with the high bit set display as 
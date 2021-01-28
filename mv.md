the mv command used to rename file or group of files as well as directories and move files from one directory to another directory 

**Syntax**

`mv [options] source dest`

option | description
-------|------------
mv -f	|force move by overwriting destination file without prompt
mv -i	|interactive prompt before overwrite
mv -u	|update - move when source is newer than destination
mv -v	|verbose - print source and destination files

**Examples:-** 
- mv test.txt new.txt
- mv src dest ( folder rename )
- mv text.txt test/ ( moving a file inside test folder) 
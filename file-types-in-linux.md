# How many types of file are there in Linux/Unix?

By default Unix have only 3 types of files. They are..

* **Regular files**
 
 These are the files which are indicated with "-" in ls -l command output at the starting of the line. And these files are.
 1. Readable file or

 2. A binary file or

 3. Image files or

 4. Compressed files etc.
```
        -rw-r--r-- 1 abc abc 20986522 2010-01-31 13:48 test.wmv
	-r-xr-xr-x 1 root root 135168 2009-12-12 19:14 VIDEO_TS.VOB
	-rwxrwxrwx 1 root root 168 2010-02-14 14:12 xyz.sh
```
* **Directory files**

These type of files contains regular files/folders/special files stored on a physical device. And this type of files will be in blue in color with link greater than or equal 2.

```
        drwxr-xr-x 2 surendra surendra 4096 2010-01-19 18:37 bin
	drwxr-xr-x 5 surendra surendra 4096 2010-02-15 18:46 Desktop
	drwxr-xr-x 2 surendra surendra 4096 2010-01-18 14:36 Documents
	drwxr-xr-x 2 surendra surendra 4096 2010-02-13 17:45 Downloads
```

* **Special files(This category is having 5 sub types in it.)**

__Block file(b)__,
__Character device file(c)__,
__Named pipe file or just a pipe file(p)__,
__Symbolic link file(l)__,
__Socket file(s)__

So in practical we have total 7 types(1+1+5) of files in Linux/Unix. And in Solaris we have 8 types. And you can see the file type indication at leftmost part of “ls -l” command.




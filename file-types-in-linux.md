# How many types of file are there in Linux/Unix?

By default Unix have only 3 types of files. They are..

* **Regular files**
 
 These are the files which are indicated with "-" in ls -l command output at the starting of the line. And these files are.
 1. Readable file or

 2. A binary file or

 3. Image files or

 4. Compressed files etc.
```
        -rw-r--r-- 1 abc abc 20986522 2020-01-31 13:48 test.wmv
	-r-xr-xr-x 1 root root 135168 2020-12-12 19:14 VIDEO_TS.VOB
	-rwxrwxrwx 1 root root 168 2020-02-14 14:12 xyz.sh
```
* **Directory files**

These type of files contains regular files/folders/special files stored on a physical device. And this type of files will be in blue in color with link greater than or equal 2.

```
        drwxr-xr-x 2 surendra surendra 4096 2020-01-19 18:37 bin
	drwxr-xr-x 5 surendra surendra 4096 2020-02-15 18:46 Desktop
	drwxr-xr-x 2 surendra surendra 4096 2020-01-18 14:36 Documents
	drwxr-xr-x 2 surendra surendra 4096 2020-02-13 17:45 Downloads
```

* **Special files(This category is having 5 sub types in it.)**

__Block file(b)__,
__Character device file(c)__,
__Named pipe file or just a pipe file(p)__,
__Symbolic link file(l)__,
__Socket file(s)__

1. block file 

These files are hardware files most of them are present in /dev.
```
        brw-rw---- 1 root disk 8, 1 2020-02-15 09:35 sda1
	brw-rw---- 1 root disk 8, 2 2020-02-15 09:35 sda2
	brw-rw---- 1 root disk 8, 5 2020-02-15 09:35 sda5
```

2. CHARACTER DEVICE FILES

Provides a serial stream of input or output.Your terminals are classic example for this type of files.
```
        crw-rw-rw- 1 root tty 5, 0 2020-02-15 16:52 tty
	crw--w---- 1 root root 4, 0 2020-02-15 09:35 tty0
	crw------- 1 root root 4, 1 2020-02-15 09:35 tty1
```

3. pipe files 

The other name of pipe is a “named” pipe, which is sometimes called a FIFO. FIFO stands for “First In, First Out” and refers to the property that the order of bytes going in is the same coming out. The “name” of a named pipe is actually a file name within the file system.
```
        prw-r----- 1 root root 0 2020-02-15 09:35 /dev/.initramfs/usplash_outfifo
	prw-r----- 1 root root 0 2020-02-15 09:35 /dev/.initramfs/usplash_fifo
	prw------- 1 syslog syslog 0 2020-02-15 15:38 /var/run/rsyslog/kmsg
```

4. symbolic link files 

These are linked files to other files. They are either Directory/Regular File. The inode number for this file and it’s parent files are same. There are two types of link files available in Linux/Unix ie soft and hard link.

```
        lrwxrwxrwx 1 root root 24 2020-02-15 09:35 sndstat -> /proc/asound/oss/sndstat
	lrwxrwxrwx 1 root root 15 2020-02-15 09:35 stderr -> /proc/self/fd/2
	lrwxrwxrwx 1 root root 15 2020-02-15 09:35 stdin -> /proc/self/fd/0
	lrwxrwxrwx 1 root root 15 2020-02-15 09:35 stdout -> /proc/self/fd/1
```
5. socket files 
A socket file is used to pass information between applications for communication purpose

```
        srwxrwxrwx 1 root root 0 2010-02-15 10:07 /var/run/cups/cups.sock
	srwxrwxrwx 1 root root 0 2010-02-15 09:35 /var/run/samba/winbindd_privileged/pipe
	srwxrwxrwx 1 mysql mysql 0 2010-02-15 09:35 /var/run/mysqld/mysqld.sock
```

So in practical we have total 7 types(1+1+5) of files in Linux/Unix. And in Solaris we have 8 types. And you can see the file type indication at leftmost part of “ls -l” command.




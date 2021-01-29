cmp command in Linux/UNIX is used to compare the two files byte by byte and helps you to find out whether the two files are identical or not.

- When cmp is used for comparison between two files, it reports the location of the first mismatch to the screen if difference is found and if no difference is found i.e the files compared are identical.
- cmp displays no message and simply returns the prompt if the the files compared are identical.

**Syntax:**
```
cmp [OPTION]... FILE1 [FILE2 [SKIP1 [SKIP2]]]

SKIP1 ,SKIP2 & OPTION are optional 
and FILE1 & FILE2 refer to the filenames 
```

Short Option	|Long Option	|Option Description
----------------|---------------|------------------
-b	|–print-bytes	|Print differing bytes.
-i SKIP	|–ignore-initial=SKIP|	Skip the first SKIP bytes of input
-i SKIP1:SKIP2|	–ignore-initial=SKIP1:SKIP2|	Skip the first SKIP1 bytes of FILE1 and the first SKIP2 bytes of FILE2.
-|–no-preserve-root|	do not treat `/’ specially (the default)
-l	|–verbose	|Output byte numbers and values of all differing bytes.
-n LIMIT|	–bytes=LIMIT|	Compare at most LIMIT bytes.
-s|	–quiet –silent	|Output nothing; yield exit status only.
-v|	–version|	Output version info.
-|–help|	Output this help.
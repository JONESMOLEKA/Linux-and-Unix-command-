# Redirection operators

symbol | Description 
-------|------------
'<'  | input redirection
  '>'  | output redirection
'2>' | error redirection 
'>>' | append redirection 

## Input redirection (<)

Instead of accepting input from standard i/p(Keyboard) we can change it to file 

**Example:-** 
- cat < myfile , will work same as cat myfile
- < indicates take input from myfile and display output on standard output device 

## Output redirection (>)

To redirect output for some file use >

**Example:-**
- cat < myfile > newfile
- ls -l > newfile

**NOTE** - if you are redirecting output to file which has already content, then the content will be overridden 

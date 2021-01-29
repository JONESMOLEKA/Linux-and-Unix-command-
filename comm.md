The comm command compares two sorted files, it gives 3 columnar output 

- first column contains lines unique to the first file 
- second column contains lines unique to the second file 
- third column displays the common lines 

**syntax**
```
comm [options]... File1 File2
```

Options	| Function
--------|---------
-1	|Does not display column 1 (does not display lines found only in file1).
-2	|Does not display column 2 (does not display lines found only in file2).
-3	|Does not display column 3 (does not display lines found in both files).
-i	|Case insensitive comparison of lines.
--check-order	|Check the order of the input, even if all input lines are pairable
--nocheck-order	|Ignore the order of the input
--output-delimiter=STR|	delimates columns with delimeter “STR”
--help	|Displays a help menu
--version	|Display command version information

**Examples**

- $ cat words.txt
```
Apple
Banana
Orange
India
US
Canada
```
- $ cat countries.txt
```
India
US
Canada
```
- $ comm -23 < (sort words.txt | uniq) < (sort countries.txt | uniq)
```
Apple 
Banana
Orange
```
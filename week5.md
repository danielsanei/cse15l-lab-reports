# Week 5 Lab Report - Researching Commands
**Daniel Sanei**

*This report describes 4 applications of the `grep` command within bash command line.*

---
## 1) Case Insensitive Search
The `grep -i "[string]" [file]` command highlights all case insensitive matches of a particular string in red.

> **Example 1 `grep -i "itALy" WhereToItaly.txt`**

![#11](https://user-images.githubusercontent.com/122568617/218643384-ff20f7f4-ff44-4208-8a5e-2c49263bb208.JPG)

> **Example 2 `grep -i "WITH" Portugal-WhatToDo.txt`**

![#22](https://user-images.githubusercontent.com/122568617/218643407-2b5b810e-f96c-475d-bb4f-18abfc31dbd2.JPG)

This command could be useful when searching for a file by keywords, but unsure of the file creator's preference for naming and formatting files (i.e. use of capitalization, special characters, abbreviations, etc).

*Source:*  https://www.geeksforgeeks.org/grep-command-in-unixlinux/

---

## 2) Word Search w/ Line Number
The `grep -n "[string]" [file]` command displays the line number and full line of a particular string, highlighting all exact matches of that string in red.


> **Example 1 `grep -n "city" HandRMadrid.txt`**

![#33](https://user-images.githubusercontent.com/122568617/218643665-38fe0978-1441-4406-800d-00f6e84b51fe.JPG)

> **Example 2 `grep -n "Portugal" IntroMadeira.txt`**

![#44](https://user-images.githubusercontent.com/122568617/218643671-e5316a7d-52dc-4ce4-b44b-6598213e3984.JPG)

This command is helpful when you know what keyword you want to find, but want the location of the word rather than just the name of the file it is contained in. The context surrounding that word may be important, and to sift through hundreds or even thousands of lines in the file is an inefficient use of time.

*Source:*  https://www.geeksforgeeks.org/grep-command-in-unixlinux/

---

## 3) Word Search w/ Any # of Lines Before/After
The `grep -A[# of lines] [string] [file]` command displays the full line containing a particular string (highlighting all exact matches of that string in red), as well as any specified number of lines occurring after said full line.
The `grep -B[# of lines] [string] [file]` command similarly displays the full line with some specific string, and any specified number of lines occurring before said full line.
The `grep -C[# of lines] [string] [file]` command is a mix of the previous two commands, displaying the full line and any specified number of lines occurring before and after said full line.

> **Example 1 `grep -A1 tourist Barcelona-WhatToDo.txt`**

![Specific Lines Search #1](https://user-images.githubusercontent.com/122568617/218641462-c4b3995c-39a0-4abc-8992-9b2a38967cb6.JPG)


> **Example 2 `grep -B0 train Paris-WhereToGo.txt`**
> 
![Specific Lines Search #2](https://user-images.githubusercontent.com/122568617/218641477-a57fab70-b3cb-4797-b43a-e056260a8640.JPG)

This command is more specific than simply finding the entire line containing a keyword, but can be useful if a specific number of lines before or after the keyword is needed (i.e. for additional context and not just the targeted line).

*Source:*  https://www.geeksforgeeks.org/grep-command-in-unixlinux/

---

## 4) Inverted Pattern Matching
The `grep -v "[string]" [file]` command displays all lines that do not contain a given string.


> **Example 1 `grep -v "a" California-WhatToDo.txt`**

![Inverted Pattern Match #1](https://user-images.githubusercontent.com/122568617/218642226-c61ac1b7-083c-4dc3-bb38-df2ec69249ed.JPG)

> **Example 2 `grep -v "the" WhatToEgypt.txt`**

![Inverted Pattern Match #2](https://user-images.githubusercontent.com/122568617/218642250-ebc51b3c-18c3-41a0-b70d-779fa1bdb80f.JPG)

This file can prove to be very helpful when seeking a file that does not contain a specific pattern, rather than searching for one that does. It is not always the case that you know exactly what you are looking for, and sometimes the case that you know what you are not looking for.

*Source:*  https://www.geeksforgeeks.org/grep-command-in-unixlinux/

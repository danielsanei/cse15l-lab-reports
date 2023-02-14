# Week 5 Lab Report - Researching Commands
**Daniel Sanei**

*This report describes 4 applications of the `grep` command within bash command line.*

---
## 1) Case Insensitive Search
The `grep -i "[string]" [file]` command highlights all case insensitive matches of a particular string in red.

> **Example 1 `grep -i "itALy" WhereToItaly.txt`**

![Case Insensitive Search #1](https://user-images.githubusercontent.com/122568617/218639445-0351f08e-0cf2-4c16-a591-53d2a538f9da.JPG)

> **Example 2 `grep -i "WITH" Portugal-WhatToDo.txt`**

![Case Insensitive Search #2](https://user-images.githubusercontent.com/122568617/218639435-195066f7-d692-45cd-adcf-8e94e2b27f55.JPG)


---

## 2) Word Search w/ Line Number
The `grep -n "[string]" [file]` command displays the line number and full line of a particular string, highlighting all exact matches of that string in red.


> **Example 1 `grep -n "city" HandRMadrid.txt`**

![Line Number Word Search #1](https://user-images.githubusercontent.com/122568617/218641249-39763799-fc04-4081-a33b-f6fdc06324cf.JPG)


> **Example 2 `grep -n "Portugal" IntroMadeira.txt`**

![Line Number Word Search #2](https://user-images.githubusercontent.com/122568617/218641264-df157554-7753-4c43-9988-afed914f5012.JPG)

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

---

## 4) Inverted Pattern Matching
The `grep -v "[string]" [file]` command displays all lines that do not contain a given string.


> **Example 1 `grep -v "a" California-WhatToDo.txt`**

![Inverted Pattern Match #1](https://user-images.githubusercontent.com/122568617/218642226-c61ac1b7-083c-4dc3-bb38-df2ec69249ed.JPG)

> **Example 2 `grep -v "the" WhatToEgypt.txt`**

![Inverted Pattern Match #2](https://user-images.githubusercontent.com/122568617/218642250-ebc51b3c-18c3-41a0-b70d-779fa1bdb80f.JPG)

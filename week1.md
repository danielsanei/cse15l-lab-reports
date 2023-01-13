# Week 1 Lab Report - Remote Access
**Daniel Sanei**

*This report describes the steps for logging into a UCSD course-specific account.*

## 1) Installing VSCode
Use the following link to install Visual Studio Code:
[Link](https://code.visualstudio.com/)

Download the version appropriate for your operating system, and open the application.
The window should look something like this:

![VSCode Screenshot](https://user-images.githubusercontent.com/122568617/212185377-9e17aa57-8444-4119-9b3c-adef2524a70c.PNG)

## 2) Remotely Connecting
If not already installed on your system, use the following links to download Git and Bash:

Git: [Link](https://gitforwindows.org/)

Bash: [Link](https://stackoverflow.com/a/50527994)

Note: Follow the extra steps in the second link to change the terminal from default to bash.

Next, open a New Terminal in VSCode (using the dropdown menu for Terminal, select New Terminal), and enter the following command, `$ ssh cs15lwi23USER@ieng6.ucsd.edu` where instead of USER, enter the respective letters in your course-specific account.
The result should include a lot of lines, and scrolling down far enough it should look something like this:

![Login Screenshot](https://user-images.githubusercontent.com/122568617/212186642-1362ed4c-535d-492b-9a0a-702fd00c8055.PNG)

This indicates your has successfully been connected to a remote computer.

## 3) Trying Some Commands
Now that your terminal is set, experiment with some of the following commands (or any others you know):

* cd
* ls
* pwd
* mkdir
* cp

As an example, the command `ls -lat` should display something like this:

![Part 5 Screenshot](https://user-images.githubusercontent.com/122568617/212211336-6c255991-5c7e-48ae-b51e-ad172ad170c8.PNG)

# Penetration_Testing_Journey
A verifiable, hands-on penetration testing portfolio covering Linux, networking, web applications, APIs, Active Directory, and cloud security
Over The Wire-Bandit Walkthrough
    level 0
  The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.
use SSH bandit0@bandit.labs.overthewire.org
  Password: bandit0
  
    L1 
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. 
Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
solved:
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
<img width="1600" height="900" alt="Screenshot (1096)" src="https://github.com/user-attachments/assets/4d886cf8-042c-40ef-8fe2-1551296c5a7d" />


   L2
   Level Goal
The password for the next level is stored in a file called - located in the home directory
key commands used are ls and cat
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat _
cat: _: No such file or directory
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cd ./-
-bash: cd: ./-: Not a directory
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ ls -la ./-
-rw-r----- 1 bandit2 bandit1 33 Sep 26 21:54 ./-
bandit1@bandit:~$ cat bandit2
cat: bandit2: No such file or directory
bandit1@bandit:~$ ls bandit2
ls: cannot access 'bandit2': No such file or directory
bandit1@bandit:~$ cat ./-
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/48dcc7ca-fce3-48e5-80db-77758b7961f0" />

  L3
  Level Goal
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory
this level show how to access files with spaces in their names
bandit2@bandit:~$ cat spaces/in/this/filename
cat: spaces/in/this/filename: No such file or directory
bandit2@bandit:~$ ls
--spaces in this filename--
bandit2@bandit:~$ cd "--spaces in this filename--
> "
-bash: cd: --: invalid option
cd: usage: cd [-L|[-P [-e]]] [-@] [dir]
bandit2@bandit:~$ cd "spaces in this filename" 
-bash: cd: spaces in this filename: No such file or directory
bandit2@bandit:~$ ls
--spaces in this filename--
bandit2@bandit:~$ cat "--spaces in this filename--"
error: unexpected argument '--spaces in this filename--' found

  tip: to pass '--spaces in this filename--' as a value, use '-- --spaces in this filename--'

Usage: cat [OPTION]... [FILE]...

For more information, try '--help'.
bandit2@bandit:~$ cat '-- --spaces in this filename--'
error: unexpected argument '-- --spaces in this filename--' found

  tip: to pass '-- --spaces in this filename--' as a value, use '-- -- --spaces in this filename--'

Usage: cat [OPTION]... [FILE]...

For more information, try '--help'.
bandit2@bandit:~$ --help
--help: command not found
bandit2@bandit:~$ cat -- "--spaces in this filename--"
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

    **Level 3**
  Level Goal
The password for the next level is stored in a hidden file in the inhere directory.
accessing hidden files in a directory
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ cd --
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Sep 26 21:54 .
drwxr-xr-x 3 root    root    4096 Sep 26 21:54 ..
-rw-r----- 1 bandit4 bandit3   33 Sep 26 21:54 ...Hiding-From-You
bandit3@bandit:~/inhere$ can hiding-from-you
Command 'can' not found, but there are 21 similar ones.
bandit3@bandit:~/inhere$ cat Hiding-From-You
cat: Hiding-From-You: No such file or directory
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq


   ** Level 4**
  The password for the next level is stored in the only human-readable file in the inhere directory.
  tip: try specifying the file type -readable
  

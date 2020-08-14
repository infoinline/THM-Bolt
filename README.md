# THM-Bolt
https://tryhackme.com/room/bolt

TryHackMe Write Up Bolt by InfoinLine @i_mline


Welcome to my first write up on TryHackMe.

******************************************************************************************************************************************************************


First scan the IP Address given to you for this room eg. nmap -sC -sV 10.10.26.72 -oN "File Name for Saved Scan" -Pn

******************************************************************************************************************************************************************

PORT     STATE SERVICE VERSION

22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)

80/tcp   open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)|_http-title: Apache2 Ubuntu Default Page: It works

8000/tcp open  http    (PHP 7.2.32-1)

******************************************************************************************************************************************************************


QUESTION #1 What port number has a webserver with a CMS running.

TIP: Now you can see that port 22 is for SSH so try ports 80 and 8000.

******************************************************************************************************************************************************************

Question #2 What is the username we can find in the CMS?

TIP: Take a look through the text on the page. See anything?

******************************************************************************************************************************************************************

Questions #3 What is the password we can find for the username?

TIP: Again have a look through the text on the webpage.

******************************************************************************************************************************************************************

Question #4 What version of the CMS is installed on the server? (Ex: Name 1.1.1)

TIP: Google what the login page url is for a Bolt CMS the once you have found that login with the username and password you found earlier.

******************************************************************************************************************************************************************

Question #5 There's an exploit for a previous version of this CMS, which allows authenticated RCE. Find it on Exploit DB. Whats its EDB-ID?

TIP: Search on Google for Exploit DB then in Exploit DB search for BOLT. Remeber what version is running on the THM server and look for the one that is the version before.

******************************************************************************************************************************************************************

Question #6 Metasploit recently added an exploit module for this vulnerability. What's the full path for this exploit? (Ex: exploit/....)
Note: If you can't find the exploit module its most likely because your metasploit isn't updated. Run `apt update` then `apt install metasploit-framework` 

TIP: exploit/unix/webapp/b**t_a************_r**

******************************************************************************************************************************************************************

Question #7  Set the LHOST, LPORT, RHOST, USERNAME, PASSWORD in msfconsole before running the exploit
TIP: Make sure everything is correct before running exploit/run

******************************************************************************************************************************************************************

Question #8 Look for flag.txt inside the machine.

TIP: cd /home

******************************************************************************************************************************************************************

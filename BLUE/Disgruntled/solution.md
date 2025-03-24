Room Access: https://tryhackme.com/room/disgruntled

## Task 1: Introduction

Hey, kid! Good, you’re here!

Not sure if you’ve seen the news, but an employee from the IT department of one of our clients (CyberT) got arrested by the police. The guy was running a successful phishing operation as a side gig.

CyberT wants us to check if this person has done anything malicious to any of their assets. Get set up, grab a cup of coffee, and meet me in the conference room.


## Task 2: Linux Forensics Review

This room requires basic knowledge of Linux and is based on the Linux Forensics room.

## Task 3: Nothing suspicious... So far

Checking the IT's guy machine

### Q1: The user installed a package on the machine using elevated privileges. According to the logs, what is the full COMMAND?
In order to find the activity perform by the user the command  ``` /var/log/auth.log ``` (explain better why auth.log)
Furthermore, we have to add the command cat to visualize what's inside the document. Since the document is so extensive, we use the grep command to filter what we want to look for, in this case, we ar elooking for an installation. Therefore, the final command is ``` cat /var/log/auth.log | grep install ``` (attach image 1)

From the image attached above, we can see that we get as an output three variables, where two are identical. 
    
    /usr/bin/apt install dokuwiki



### Q2: What was the present working directory (PWD) when the previous command was run?
    /home/cybert
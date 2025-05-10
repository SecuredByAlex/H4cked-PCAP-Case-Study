# H4cked-analysis

## Objective
To simulate the role of a SOC analyst by investigating a network compromise scenario provided in the TryHackMe "H4cked" room. The focus is on analyzing a .pcap file to identify signs of brute-force attacks, malicious file uploads, and suspicious reverse shell activity—all without performing any offensive exploitation.

## Skilled Learned
- Network traffic analysis using Wireshark
- Detection of brute-force login attempts via FTP
- Identification of web shell uploads (shell.php)
- Recognition of reverse shell behavior in captured traffic
- Extraction of Indicators of Compromise (IOCs)

## Tools Used 
- Wireshark – for PCAP traffic inspection
- TryHackMe – H4cked Room – structured cybersecurity lab

## Scenario
It seems like our machine got hacked by an anonymous threat actor. However, we are lucky to have a .pcap file from the attack. Can you determine what happened? Download the .pcap file and use Wireshark to view it.

## Steps Taken
Q1. The attacker is trying to log into a specific service. What service is this?<br>
Ans: FTP<br>
O/P: <img src="https://github.com/user-attachments/assets/e9889db8-2544-47bc-9434-c84181669cf7" /><br><br>


Q2. There is a very popular tool by Van Hauser which can be used to brute force a series of services. What is the name of this tool?<br>
Ans: Hydra<br><br>


Q3. The attacker is trying to log on with a specific username. What is the username?<br>
Ans: Jenny<br>
O/P: <img src="https://github.com/user-attachments/assets/06bf2dfa-8622-4421-b679-205e10355476" /><br><br>


Q4. What is the user's password?<br>
Ans: password123<br>
O/P: <img src="https://github.com/user-attachments/assets/831a9d39-84fc-4d7b-a994-20b977f1774c" /><br><br>


Q5. What is the current FTP working directory after the attacker logged in?<br>
Ans: /var/www/html<br>
O/P: <img src="https://github.com/user-attachments/assets/bb0aa014-f73d-4be0-8026-62cb2f6d0089" /><br><br>


Q6. The attacker uploaded a backdoor. What is the backdoor's filename?<br>
Ans: shell.php<br>
O/P: <img src="https://github.com/user-attachments/assets/0eebb8af-a787-4b7a-8801-b0ebf54d578e" /><br><br>


Q7. The backdoor can be downloaded from a specific URL, as it is located inside the uploaded file. What is the full URL?<br>
Ans: http://pentestmonkey.net/tools/php-reverse-shell<br>
O/P: <img src="https://github.com/user-attachments/assets/2c89cd23-53a7-4231-a4e8-13b26b0a84cf" /><br><br>

Q8. Which command did the attacker manually execute after getting a reverse shell?<br>
Ans: whoami<br>
O/P: <img src="https://github.com/user-attachments/assets/3201bead-d20f-4807-bf95-916448869016" /><br><br>


Q9. What is the computer's hostname?<br>
Ans: wir3<br>
O/P: <img src="https://github.com/user-attachments/assets/282d44fb-604f-4f9e-8680-37d17c29b11b" /><br><br>


Q10. Which command did the attacker execute to spawn a new TTY shell?<br>
Ans: python3 -c 'import pty; pty.spawn("/bin/bash")'<br>
O/P: <img src="https://github.com/user-attachments/assets/5d10fe9c-b257-4afc-ab1e-2d4d3a470a04" /><br><br>

Q11. Which command was executed to gain a root shell?<br>
Ans: sudo su<br>
O/P: <img src="https://github.com/user-attachments/assets/3120ab7f-91c4-436f-a8f3-8ecb231052c1" /><br><br>

Q12. The attacker downloaded something from GitHub. What is the name of the GitHub project?<br>
Ans: Reptile<br>
O/P: <img src="https://github.com/user-attachments/assets/7fc8a50a-0db2-480b-ba61-063e97333621" /><br><br>

Q13. The project can be used to install a stealthy backdoor on the system. It can be very hard to detect. What is this type of backdoor called?<br>
Ans: Rootkit<br>
O/P: <img src="https://github.com/user-attachments/assets/8a78c889-d07d-4eab-88b1-9628eb084ad8" /><br><br>

## Conclusion
This project, based on Task 1 of the TryHackMe "H4cked" room, offered hands-on experience in identifying and interpreting signs of network compromise. Through careful analysis of packet data, I was able to trace attacker actions including FTP brute-force attempts, file upload of a malicious PHP shell, and the establishment of a reverse shell. These findings were documented using SOC best practices and mapped to real-world adversary techniques via MITRE ATT&CK. The exercise deepened my understanding of network forensics and enhanced my readiness for real-world SOC analyst responsibilities.

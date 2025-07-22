# Network-Traffic-Wireshark-
<h2>Description</h2>
A single port scan alert led to uncovering a complete internal attack chain—executed in under 10 minutes. Using Wireshark and packet analysis, I confirmed successful exploitation and remote access by the attacker.

Attack Chain Breakdown
Recon
10.251.96.4 scanned 10.251.96.5 on ports 22 & 80

Timestamp: 2021-02-07 16:33:06

Enumeration

Gobuster identified /upload and other paths

Tool: Gobuster v3.0.1

Exploitation

SQLmap launched automated SQL injection

Database info enumeration observed

Persistence

Web shell (functions.php) uploaded via exposed endpoint

Timestamp: 2021-02-07 16:40:39

Command & Control

Reverse shell from 10.251.96.5 → 10.251.96.4

Commands: id, whoami, Python callback

Tools & Techniques
Wireshark for full PCAP analysis

Manual TCP stream inspection

Behavior signature analysis (Gobuster & SQLmap)

<br />
<h2> Utilities Used</h2>
- <b>VM WORKSTATION</b> 

<h2>Program walk-through:</h2>

<p align="center">
 <br/>
<br /> <img src="https://i.imgur.com/Y38hWpG.png" height="80%" width="80%" alt="Protocol"/>
<br />
<img src="https://i.imgur.com/1c0s1gg.png" height="80%" width="80%" alt="Protocol"/>
<br />
<br />
<img src="https://i.imgur.com/i4UxuVa.png" height="80%" width="80%" alt="Source"/>
<br /> 
<img src="https://i.imgur.com/vJ5VrJz.png" height="80%" width="80%" alt="Source"/>
<br />

# Dual Threat Analysis: Email Exploits And Rce Attacks 
Project Title: Dual Threat Analysis: Email Exploits And Rce Attacks 
<br>Course project: Information Warfare
## describe
**Role:** Team Leader (5 members) - Deploying and analyzing RCE attacks. 
<br>**Objectives:** 
- Analyze and execute two attack scenarios: Email attacks and Remote Code Execution (RCE) in a secure testing environment. 
- Analyze malware samples and propose security measures.

<br>**Programming Languages:** PHP, Bash (Shell Scripting), NSIS Script. 
<br>**Tools:** Metasploit, Wireshark, Zphisher, Burp Suite, Sophos Home. 
<br>**Virtualization Platform:** VMware | **OS:** Kali Linux, Windows 10.

### Topic summary:
This project aims to understand and analyze two common attack scenarios in the cyber world: email attacks and attacks using hijacking techniques (RCE). We will execute these attacks in a secure test environment, in conjunction with malware sample analysis and deployment of corresponding defensive measures. The objective of the project is to provide specific security recommendations and solutions, helping to enhance the safety and protection of information systems
### Idel about atack RCE
**RCE attack model**
![ RCE attack model](https://github.com/nnc-11/Dual-Threat-Analysis-Email-Exploits-And-Rce-Attacks-/blob/72a476a0398d96421e2ddb61fae29d291b28b699/RCE%20attack%20model.png)

Create a game download file through the pikachu game download program, to inject the payload.exe file hidden as pikachu update the necessary file for the game program.
<br>**Minimize suspicion by:**
<br>Just download the game and use it, no need to do anything.
<br>Do not require turning off REA_TIME PROTECTION.
- Use Metasploit Framework to create the payload.exe file
- Rename the payload.exe file -> pikachuupdate.exe
- Write NSIS script: the writing process helps to bypass read-time protection and the payload file is not deleted by windows protection.
  - Download all necessary files to the game folder.
  - Put that folder in the EXCLUSION folder.
  - Execute Pikachu.exe (safe game program -> distract) at this time the user will play the game after downloading.
  - Execute Pikachuupdate.exe (payload), note: EXCLUSION script must be written first.
- At this time, after the execution process is complete, a session connection occurs. RCE successful. Continue creating backdoors, and increase payload lifetime.
## file
- 'informationWarfare_CMU-CS426BIS_ProjectGroup4.pdf':final report
- 'informationWarfare_CMU-CS426BIS_ProjectGroup4.pdf':final report
- 'Lenh_RCE.txt': Some successful RCE attack exploits
- nsis_cript.txt': Custom script installation steps

# **Metasploit**
Фреймворк для эксплойтов, набор инструментов с открытым исходным кодом, используемых для анализа сетей, выявления уязвимостей, разработки полезной нагрузки и выполнения кода эксплойта на удаленных целевых машинах.

## **Link**
- [Metasploit](https://www.metasploit.com/)
- [Rooms](https://tryhackme.com/r/module/metasploit)

## **Content**
### **Metasploit: Introduction**
#### **Task 2**
- What is the name of the code taking advantage of a flaw on the target system?  
	Exploit

- What is the name of the code that runs on the target system to achieve the attacker's goal?
	Payload

- What are self-contained payloads called?  
	Singles

- Is "windows/x64/pingback_reverse_tcp" among singles or staged payload?  
	Singles

#### **Task 3**
- How would you search for a module related to Apache?
	search apache

- Who provided the auxiliary/scanner/ssh/ssh_login module?
	todb

#### **Task 4**
- How would you set the LPORT value to 6666?
	set LPORT 6666
- How would you set the global value for RHOSTS  to 10.10.19.23 ?
	setg RHOSTS 10.10.19.23

- What command would you use to clear a set payload?
	unset PAYLOAD

- What command do you use to proceed with the exploitation phase?
	exploit

### **Metasploit:  Exploitation**
#### **Task 2**
- How many ports are open on the target system?
	5

- Using the relevant scanner, what NetBIOS name can you see?
	ACME IT SUPPORT

- What is running on port 8000?
	webfs/1.21

- What is the "penny" user's SMB password? Use the wordlist mentioned in the previous task.
	leo1234

#### **Task 4**
- Who wrote the module that allows us to check SMTP servers for open relay?
	Campbell Murray

#### **Task 5**
- What is the content of the flag.txt file?
	 THM-5455554845

- What is the NTLM hash of the password of the user "pirate"?
	 8ce9a3ebd1647fcc5e04025019f4b875
#### **Task 6**
- What is the other user's password hash?	
- \$6\$Sy0NNIXw$SJ27WltHI89hwM5UxqVGiXidj94QFRm2Ynp9p9kxgVbjrmtMez9EqXoDWtcQd8rf0tjc77hBFbWxjGmQCTbep0

### **Metasploit: Meterpreter**
#### **Task 2**
- How many ports are open on the target system?
	5

- Using the relevant scanner, what NetBIOS name can you see?
	ACME IT SUPPORT

- What is running on port 8000?
	webfs/1.21

- What is the "penny" user's SMB password? Use the wordlist mentioned in the previous task.
	leo1234

#### **Task 4**
- Who wrote the module that allows us to check SMTP servers for open relay?
	Campbell Murray

#### **Task 5**
- What is the content of the flag.txt file?
	 THM-5455554845

- What is the NTLM hash of the password of the user "pirate"?
	 8ce9a3ebd1647fcc5e04025019f4b875
#### **Task 6**
- What is the other user's password hash?	
- \$6\$Sy0NNIXw$SJ27WltHI89hwM5UxqVGiXidj94QFRm2Ynp9p9kxgVbjrmtMez9EqXoDWtcQd8rf0tjc77hBFbWxjGmQCTbep0


# **Metasploit**
Фреймворк для эксплойтов, набор инструментов с открытым исходным кодом, используемых для анализа сетей, выявления уязвимостей, разработки полезной нагрузки и выполнения кода эксплойта на удаленных целевых машинах.

## **Link**
- [Metasploit](https://www.metasploit.com/)
- [Rooms](https://tryhackme.com/r/module/metasploit)

## **Contents**
### **Введение**
#### **Основные понятия:**
- **Консоль** - основной интерфейс для взаимодействия с различными модулями Metasploit Framework.
- **Модули** - это небольшие компоненты фреймворка Metasploit, созданные для выполнения определенной задачи, такой как эксплуатация уязвимости, сканирование цели или проведение брутфорс-атаки.
- **Exploit** - часть кода, которая использует уязвимость, присутствующую в целевой системе.
- **Vulnerability** - дефект проектирования, кодирования или логики, влияющий на целевую систему. Эксплуатация уязвимости может привести к раскрытию конфиденциальной информации или позволить злоумышленнику выполнить код на целевой системе.
- **Payload** - эксплойт использует уязвимость в своих интересах. Однако если мы хотим, чтобы эксплойт привел к желаемому результату (получение доступа к целевой системе, чтение конфиденциальной информации и т. д.), нам необходимо использовать полезную нагрузку. Полезная нагрузка - это код, который будет выполняться на целевой системе. 

#### **Модули и категории:**
-  **Auxiliary** - модули, сканеры, краулеры и фаззеры;
```bash
/opt/metasploit-framework/embedded/framework/modules# tree -L 1 auxiliary/
```
- **Encoders** - позволяют зашифровать эксплойт и полезную нагрузку в надежде, что сигнатурные антивирусы не смогут их выявить;
``` bash
/opt/metasploit-framework/embedded/framework/modules# tree -L 1 encoders/
```
- **Evasion** - данные модули могут использоваться совместно с encoders и обходить СЗИ;
```
/opt/metasploit-framework/embedded/framework/modules# tree -L 2 evasion/
```
- **Exploits** -  эксплойты, организованные по целевым системам;
```
/opt/metasploit-framework/embedded/framework/modules# tree -L 1 exploits/
```
- **NOPs** -  (No OPeration) ничего не делают, в буквальном смысле. В семействе процессоров Intel x86 они обозначаются 0x90, после чего процессор ничего не делает в течение одного цикла. Они часто используются в качестве буфера для достижения постоянного размера полезной нагрузки;
```bash
/opt/metasploit-framework/embedded/framework/modules# tree -L 1 nops/
```
- **Payloads** - код, который будет запущен на целевой системе. Эксплойты используют уязвимость целевой системы, но для достижения желаемого нужна полезная нагрузка (получение shell'a, загрузка вредоносного ПО или бэкдора);
```bash
/opt/metasploit-framework/embedded/framework/modules# tree -L 1 payloads/
```
- **Post** - полезны на заключительном этапе процесса тестирования на проникновение.
```bash
/opt/metasploit-framework/embedded/framework/modules# tree -L 1 post/
```

#### **Основные команды:**
- Запуск metaspolit'a;
```bash
msfconsole
```
- Выбор эксплойта;
```bash
use exploit/windows/smb/ms17_010_eternalblue 
```
- Выход в косноль;
```bash
back 
```
- Информация об эксплойте (можно добавить имя модуля);
```bash
info
show options
show payloads
```
- Поиск;
```bash
search 
```
- Запуск эксплойта;
```bash
run
```
- Перевод сессии в фоновый режим;
```bash
background
```
- Просмотр и выбор сессии;
```bash
sessions
sessions -i
```

#### **Часто используемые переменные:**
- Задать или убрать переменную для конкретного или глобального параметра;
```bash
set
unset
setg
unsetg
```
- **RHOSTS** - IP-адрес или диапазон целевой системы;
- **RPORT** - порт целевой системы;
- **PAYLOAD** - полезная нагрузка для эксплойта;
- **LHOST** - локальный хост;
- **LPORT** - локальный порт;
- **SESSION** - каждое соединение, установленное с целевой системой с помощью Metasploit.

### **Использование**
#### **Сканирование:**
- Portscan;
- UDP service Identification (udp_sweep);
- SMB Scans (smb_version или smb_enumshares).

#### **Работа с БД:**
В Metasploit есть функция базы данных, которая упрощает управление проектом и позволяет избежать возможной путаницы при создании значений параметров.
- Инициализация:
```bash
systemctl start postgresql
msfdb init
```
- Подключение и создание рабочего пространства.
```bash
db_status
workspace -a tryhackme
```

#### ****

## **Answer the questions**
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



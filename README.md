# notes
![image](https://github.com/owocowyyogurd/notes/assets/42451598/c5092fc6-259b-4a12-b96d-52e1f1087c4a)

-T4 is for time (1 to 5 the more i give the more fast result are expected)

-A agressive

-v verbosity

-O os discovery


**Export:**

nmap -sn 70.10.0.1/24 -oN nmap.txt

nmap -O 70.10.0.1/24 -oN namp-OS.txt

namp -sC -sV -sS 70.10.0.1 -oN namp-all.txt

**Scan/Discovery**
Netdiscover -i eth

Netdiscovery -r 10.10.10.1/24


Namp -sn 192.168.x.1/24

Nmap -sn -PR 192.168.x.1-255

![image](https://github.com/owocowyyogurd/notes/assets/42451598/d1624dcc-b955-442e-8c97-9c360bc6c4b4)


**Windows**
Angry IP scanner

**Scan Service/OS**
Nmap -sP 192.168.x.*

Nmap -sC -sV -p- -T4 -v 192.168.x.*

Nmap -sC -sV -p- -O -v -A -T4 192.168.x.*



**Service**
Nmap - sS -sV 192.168.x.1/24

Hping3 -S 192.168.x.1 -p 80 -c 5



**HPING**
PortScanning using Hping3: 

hping3 --scan 1-3000 -S 10.10.10.10 --scan parameter defines the port range to scan and –S represents SYN flag.

**Pinging the target using HPing3:**

 hping3 -c 3 10.10.10.10 -c 3 means that we only want to send three packets to the target machine.

**UDP Packet Crafting**

 hping3 10.10.10.10 --udp --rand-source --data 500

**TCP SYN request **

hping3 -S 10.10.10.10 -p 80 -c 5

-S will perform TCP SYN request on the target machine, -p will pass the traffic through which port is assigned, and -c is the count of the packets sent to the Target machine.

**HPing flood**

 hping3 10.10.10.10 --flood


**OS**

Namp -sS -O 192.168.x.1/24

Sudo nmap --script smb-os-discovery.nse IP

Sudo nmap -sS -p 445 -A IP 




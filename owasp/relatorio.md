# nmap -sV -O 10.1.2.6

```
Starting Nmap 7.80 ( https://nmap.org ) at 2019-11-05 04:36 EST
Nmap scan report for 10.1.2.6
Host is up (0.00075s latency).
Not shown: 991 closed ports
PORT     STATE SERVICE     VERSION
22/tcp   open  ssh         OpenSSH 5.3p1 Debian 3ubuntu4 (Ubuntu Linux; protocol 2.0)
80/tcp   open  http        Apache httpd 2.2.14 ((Ubuntu) mod_mono/2.4.3 PHP/5.3.2-1ubuntu4.30 with Suhosin-Patch proxy_html/3.0.1 mod_python/3.3.1 Python/2.6.5 mod_ssl/2.2.14 OpenSSL...)
139/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
143/tcp  open  imap        Courier Imapd (released 2008)
443/tcp  open  ssl/https?
445/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
5001/tcp open  java-object Java Object Serialization
8080/tcp open  http        Apache Tomcat/Coyote JSP engine 1.1
8081/tcp open  http        Jetty 6.1.25
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port5001-TCP:V=7.80%I=7%D=11/5%Time=5DC142B7%P=x86_64-pc-linux-gnu%r(NU
SF:LL,4,"\xac\xed\0\x05");
MAC Address: 08:00:27:89:F3:2F (Oracle VirtualBox virtual NIC)
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6
OS details: Linux 2.6.17 - 2.6.36
Network Distance: 1 hop
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 21.46 seconds
```

# nmap -v -A 10.1.2.6

```
Starting Nmap 7.80 ( https://nmap.org ) at 2019-11-05 04:32 EST
NSE: Loaded 151 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 04:32
Completed NSE at 04:32, 0.00s elapsed
Initiating NSE at 04:32
Completed NSE at 04:32, 0.00s elapsed
Initiating NSE at 04:32
Completed NSE at 04:32, 0.00s elapsed
Initiating ARP Ping Scan at 04:32
Scanning 10.1.2.6 [1 port]
Completed ARP Ping Scan at 04:32, 0.05s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 04:32
Completed Parallel DNS resolution of 1 host. at 04:32, 0.01s elapsed
Initiating SYN Stealth Scan at 04:32
Scanning 10.1.2.6 [1000 ports]
Discovered open port 445/tcp on 10.1.2.6
Discovered open port 22/tcp on 10.1.2.6
Discovered open port 143/tcp on 10.1.2.6
Discovered open port 139/tcp on 10.1.2.6
Discovered open port 80/tcp on 10.1.2.6
Discovered open port 443/tcp on 10.1.2.6
Discovered open port 8080/tcp on 10.1.2.6
Discovered open port 8081/tcp on 10.1.2.6
Discovered open port 5001/tcp on 10.1.2.6
Completed SYN Stealth Scan at 04:32, 0.11s elapsed (1000 total ports)
Initiating Service scan at 04:32
Scanning 9 services on 10.1.2.6
Completed Service scan at 04:33, 14.04s elapsed (9 services on 1 host)
Initiating OS detection (try #1) against 10.1.2.6
NSE: Script scanning 10.1.2.6.
Initiating NSE at 04:33
Completed NSE at 04:33, 31.39s elapsed
Initiating NSE at 04:33
Completed NSE at 04:34, 60.01s elapsed
Initiating NSE at 04:34
Completed NSE at 04:34, 0.00s elapsed
Nmap scan report for 10.1.2.6
Host is up (0.00072s latency).
Not shown: 991 closed ports
PORT     STATE SERVICE     VERSION
22/tcp   open  ssh         OpenSSH 5.3p1 Debian 3ubuntu4 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   1024 ea:83:1e:45:5a:a6:8c:43:1c:3c:e3:18:dd:fc:88:a5 (DSA)
|_  2048 3a:94:d8:3f:e0:a2:7a:b8:c3:94:d7:5e:00:55:0c:a7 (RSA)
80/tcp   open  http        Apache httpd 2.2.14 ((Ubuntu) mod_mono/2.4.3 PHP/5.3.2-1ubuntu4.30 with Suhosin-Patch proxy_html/3.0.1 mod_python/3.3.1 Python/2.6.5 mod_ssl/2.2.14 OpenSSL...)
|_http-favicon: Unknown favicon MD5: 1F8C0B08FB6B556A6587517A8D5F290B
| http-methods:
|   Supported Methods: GET HEAD POST OPTIONS TRACE
|_  Potentially risky methods: TRACE
|_http-server-header: Apache/2.2.14 (Ubuntu) mod_mono/2.4.3 PHP/5.3.2-1ubuntu4.30 with Suhosin-Patch proxy_html/3.0.1 mod_python/3.3.1 Python/2.6.5 mod_ssl/2.2.14 OpenSSL/0.9.8k Phusion_Passenger/4.0.38 mod_perl/2.0.4 Perl/v5.10.1
|_http-title: owaspbwa OWASP Broken Web Applications
139/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
143/tcp  open  imap        Courier Imapd (released 2008)
|_imap-capabilities: OK completed CAPABILITY SORT ACL2=UNIONA0001 IDLE THREAD=REFERENCES IMAP4rev1 NAMESPACE QUOTA ACL THREAD=ORDEREDSUBJECT UIDPLUS CHILDREN
443/tcp  open  ssl/https?
|_ssl-date: 2019-11-05T06:33:35+00:00; -3h00m01s from scanner time.
445/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
5001/tcp open  java-object Java Object Serialization
8080/tcp open  http        Apache Tomcat/Coyote JSP engine 1.1
|_http-server-header: Apache-Coyote/1.1
|_http-title: Site doesn't have a title.
8081/tcp open  http        Jetty 6.1.25
| http-methods:
|   Supported Methods: GET HEAD POST TRACE OPTIONS
|_  Potentially risky methods: TRACE
|_http-server-header: Jetty(6.1.25)
|_http-title: Choose Your Path
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port5001-TCP:V=7.80%I=7%D=11/5%Time=5DC141C6%P=x86_64-pc-linux-gnu%r(NU
SF:LL,4,"\xac\xed\0\x05");
MAC Address: 08:00:27:89:F3:2F (Oracle VirtualBox virtual NIC)
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6
OS details: Linux 2.6.17 - 2.6.36
Uptime guess: 198.050 days (since Sun Apr 21 04:23:01 2019)
Network Distance: 1 hop
TCP Sequence Prediction: Difficulty=192 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Host script results:
|_clock-skew: mean: -3h00m01s, deviation: 0s, median: -3h00m01s
| smb-security-mode:
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
|_smb2-time: Protocol negotiation failed (SMB2)

TRACEROUTE
HOP RTT     ADDRESS
1   0.72 ms 10.1.2.6

NSE: Script Post-scanning.
Initiating NSE at 04:34
Completed NSE at 04:34, 0.00s elapsed
Initiating NSE at 04:34
Completed NSE at 04:34, 0.00s elapsed
Initiating NSE at 04:34
Completed NSE at 04:34, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 107.70 seconds
           Raw packets sent: 1020 (45.626KB) | Rcvd: 1016 (41.374KB)
```

# nmap -sS -v --top-ports 10 --reason -oA saidanmap www.ufsc.br

```
Starting Nmap 7.80 ( https://nmap.org ) at 2019-11-05 06:39 -03
Initiating Ping Scan at 06:39
Scanning www.ufsc.br (150.162.2.10) [4 ports]
Completed Ping Scan at 06:39, 0.05s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 06:39
Completed Parallel DNS resolution of 1 host. at 06:39, 0.06s elapsed
Initiating SYN Stealth Scan at 06:39
Scanning www.ufsc.br (150.162.2.10) [10 ports]
Discovered open port 443/tcp on 150.162.2.10
Discovered open port 80/tcp on 150.162.2.10
Completed SYN Stealth Scan at 06:39, 1.25s elapsed (10 total ports)
Nmap scan report for www.ufsc.br (150.162.2.10)
Host is up, received echo-reply ttl 60 (0.0089s latency).
Other addresses for www.ufsc.br (not scanned): 2801:84:0:2::10
rDNS record for 150.162.2.10: paginas.ufsc.br

PORT     STATE    SERVICE       REASON
21/tcp   filtered ftp           no-response
22/tcp   filtered ssh           no-response
23/tcp   filtered telnet        no-response
25/tcp   filtered smtp          no-response
80/tcp   open     http          syn-ack ttl 60
110/tcp  filtered pop3          no-response
139/tcp  filtered netbios-ssn   no-response
443/tcp  open     https         syn-ack ttl 60
445/tcp  filtered microsoft-ds  no-response
3389/tcp filtered ms-wbt-server no-response

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 1.49 seconds
           Raw packets sent: 22 (944B) | Rcvd: 3 (116B)
```

# Crie um comando nmap com opções diferentes das usadas nas questões anteriores e explique a saída obtida pelo seu comando

O comando criado foi `nmap -sT -sV 10.1.2.6` e sua saida foi:

```
Starting Nmap 7.80 ( https://nmap.org ) at 2019-11-05 05:43 EST
Nmap scan report for 10.1.2.6
Host is up (0.00040s latency).
Not shown: 991 closed ports
PORT     STATE SERVICE     VERSION
22/tcp   open  ssh         OpenSSH 5.3p1 Debian 3ubuntu4 (Ubuntu Linux; protocol 2.0)
80/tcp   open  http        Apache httpd 2.2.14 ((Ubuntu) mod_mono/2.4.3 PHP/5.3.2-1ubuntu4.30 with Suhosin-Patch proxy_html/3.0.1 mod_python/3.3.1 Python/2.6.5 mod_ssl/2.2.14 OpenSSL...)
139/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
143/tcp  open  imap        Courier Imapd (released 2008)
443/tcp  open  ssl/https?
445/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
5001/tcp open  java-object Java Object Serialization
8080/tcp open  http        Apache Tomcat/Coyote JSP engine 1.1
8081/tcp open  http        Jetty 6.1.25
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port5001-TCP:V=7.80%I=7%D=11/5%Time=5DC1524C%P=x86_64-pc-linux-gnu%r(NU
SF:LL,4,"\xac\xed\0\x05");
MAC Address: 08:00:27:89:F3:2F (Oracle VirtualBox virtual NIC)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 19.63 seconds
```

A saida é similar ao comando `nmap -sV -O 10.1.2.6` porem, ao passar a flag -sT forçamos o nmap a utilizar chamadas de sistema chamadas connect.

# Qual questão anterior usa scan de conexão TCP e qual questão usa SYN scan

Os comandos que utilizam TCP SYN scan:
`nmap -sV -O 10.1.2.6`;
`nmap -v -A 10.1.2.6`;
`nmap -sS -v --top-ports 10 --reason -oA saidanmap www.ufsc.br`;

Os comandos que utilizam TCP conect:
`nmap -sT -sV 10.1.2.6`.


## Install
```sudo cp -r recon /usr/bin/ && sudo chmod +x /usr/bin/recon```

```
┌──(root💀ghost)-[/home/ghost]
└─# recon          

    .o oOOOOOOOo                                            OOOo
    Ob.OOOOOOOo  OOOo.      oOOo.                      .adOOOOOOO
    OboO"""""""""""".OOo. .oOOOOOo.    OOOo.oOOOOOo.."""""""""'OO
    OOP.oOOOOOOOOOOO "POOOOOOOOOOOo.   `"OOOOOOOOOP,OOOOOOOOOOOB'
    `O'OOOO'     `OOOOo"OOOOOOOOOOO` .adOOOOOOOOO"oOOO'    `OOOOo
    .OOOO'            `OOOOOOOOOOOOOOOOOOOOOOOOOO'            `OO
    OOOOO                 '"OOOOOOOOOOOOOOOO"`                oOO
   oOOOOOba.                .adOOOOOOOOOOba               .adOOOOo.
  oOOOOOOOOOOOOOba.    .adOOOOOOOOOO@^OOOOOOOba.     .adOOOOOOOOOOOO
 OOOOOOOOOOOOOOOOO.OOOOOOOOOOOOOO"`  '"OOOOOOOOOOOOO.OOOOOOOOOOOOOO
 "OOOO"       "YOoOOOOMOIONODOO"`  .   '"OOROAOPOEOOOoOY"     "OOO"
    Y           'OOOOOOOOOOOOOO: .oOOo. :OOOOOOOOOOO?'         :`
    :            .oO%OOOOOOOOOOo.OOOOOO.oOOOOOOOOOOOO?         .
    .            oOOP"%OOOOOOOOoOOOOOOO?oOOOOO?OOOO"OOo
                 '%o  OOOO"%OOOO%"%OOOOO"OOOOOO"OOO':
                      `$"  `OOOO' `O"Y ' `OOOO'  o             .
    .                  .     OP"          : o     .
                              :
                              .

[R3C0N] by 0bfxgh0st* 4 WWA with ❤

Tcp port scan
Web services recognizement
Web services directories fuzzing (light)
Check mysql service misconfiguration root:<blank> credentials on mysql database
Check smb service no-password & shared folders enumeration
Check ftp service misconfiguration anonymous/ftp:<blank> credentials

Usage recon <host>
```
Ouput example  
```
┌──(root💀ghost)-[/home/ghost]
└─# recon ghost.server

    .o oOOOOOOOo                                            OOOo
    Ob.OOOOOOOo  OOOo.      oOOo.                      .adOOOOOOO
    OboO"""""""""""".OOo. .oOOOOOo.    OOOo.oOOOOOo.."""""""""'OO
    OOP.oOOOOOOOOOOO "POOOOOOOOOOOo.   `"OOOOOOOOOP,OOOOOOOOOOOB'
    `O'OOOO'     `OOOOo"OOOOOOOOOOO` .adOOOOOOOOO"oOOO'    `OOOOo
    .OOOO'            `OOOOOOOOOOOOOOOOOOOOOOOOOO'            `OO
    OOOOO                 '"OOOOOOOOOOOOOOOO"`                oOO
   oOOOOOba.                .adOOOOOOOOOOba               .adOOOOo.
  oOOOOOOOOOOOOOba.    .adOOOOOOOOOO@^OOOOOOOba.     .adOOOOOOOOOOOO
 OOOOOOOOOOOOOOOOO.OOOOOOOOOOOOOO"`  '"OOOOOOOOOOOOO.OOOOOOOOOOOOOO
 "OOOO"       "YOoOOOOMOIONODOO"`  .   '"OOROAOPOEOOOoOY"     "OOO"
    Y           'OOOOOOOOOOOOOO: .oOOo. :OOOOOOOOOOO?'         :`
    :            .oO%OOOOOOOOOOo.OOOOOO.oOOOOOOOOOOOO?         .
    .            oOOP"%OOOOOOOOoOOOOOOO?oOOOOO?OOOO"OOo
                 '%o  OOOO"%OOOO%"%OOOOO"OOOOOO"OOO':
                      `$"  `OOOO' `O"Y ' `OOOO'  o             .
    .                  .     OP"          : o     .
                              :
                              .

[R3C0N] by 0bfxgh0st* 4 WWA with ❤

[OS] Linux (99%)
Starting Nmap 7.92 ( https://nmap.org ) at 2022-10-20 15:44 EDT
NSE: Loaded 1 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 15:44
Completed NSE at 15:44, 0.00s elapsed
Initiating SYN Stealth Scan at 15:44
Scanning ghost.server (127.0.0.1) [65535 ports]
Discovered open port 80/tcp on 127.0.0.1
Discovered open port 139/tcp on 127.0.0.1
Discovered open port 21/tcp on 127.0.0.1
Discovered open port 3306/tcp on 127.0.0.1
Discovered open port 445/tcp on 127.0.0.1
Completed SYN Stealth Scan at 15:44, 0.50s elapsed (65535 total ports)
NSE: Script scanning 127.0.0.1.
Initiating NSE at 15:44
Completed NSE at 15:44, 0.00s elapsed
Nmap scan report for ghost.server (127.0.0.1)
Host is up (0.0000030s latency).
rDNS record for 127.0.0.1: localhost
Not shown: 65530 closed tcp ports (reset)
PORT     STATE SERVICE
21/tcp   open  ftp
|_ftp-anon: Anonymous FTP login allowed (FTP code 230)
80/tcp   open  http
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
3306/tcp open  mysql

NSE: Script Post-scanning.
Initiating NSE at 15:44
Completed NSE at 15:44, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.70 seconds
           Raw packets sent: 65535 (2.884MB) | Rcvd: 131075 (5.505MB)

┌─[+] [mysql]
└─(Credentials for mysql ghost.server:3306)
  [user:root][password:]

┌─[+] [ftp]
└─(Credentials for ftp ghost.server:21)
  [user:ftp][password:]
  [user:anonymous][password:]

[i] [SMB]
[+] IP: ghost.server:445        Name: unknown                                           
        Disk                                                    Permissions     Comment
        ----                                                    -----------     -------
        print$                                                  NO ACCESS       Printer Drivers
        Shared                                                  READ ONLY
        IPC$                                                    NO ACCESS       IPC Service (Samba 4.16.0-Debian)

        Sharename       Type      Comment
        ---------       ----      -------
        print$          Disk      Printer Drivers
        Shared          Disk      
        IPC$            IPC       IPC Service (Samba 4.16.0-Debian)
Reconnecting with SMB1 for workgroup listing.
protocol negotiation failed: NT_STATUS_INVALID_NETWORK_RESPONSE
Unable to connect with SMB1 -- no workgroup available
[print$]
tree connect failed: NT_STATUS_ACCESS_DENIED
[Shared]
Current directory is \\ghost.server\Shared\
  .                                   D        0  Thu Oct 20 13:39:38 2022
  ..                                  D        0  Thu Oct 20 15:39:19 2022
  file                                N        5  Thu Oct 20 13:39:38 2022

                73709560 blocks of size 1024. 57146168 blocks available
[IPC$]
Current directory is \\ghost.server\IPC$\
NT_STATUS_CONNECTION_REFUSED listing \*

[i] [WHATWEB]
http://ghost.server:80 [200 OK] Apache[2.4.53], Country[RESERVED][ZZ], HTTPServer[Debian Linux][Apache/2.4.53 (Debian)], IP[127.0.0.1], Title[Apache2 Debian Default Page: It works]

[+] [WFUZZ]
*stage 1 --> (light web path fuzzing wordlist:/usr/share/dirb/wordlists/common.txt)
********************************************************
* Wfuzz 3.1.0 - The Web Fuzzer                         *
********************************************************

Target: http://ghost.server:80/FUZZ
Total requests: 4614

=====================================================================
ID           Response   Lines    Word       Chars       Payload                                                                                                                           
=====================================================================

000000001:   200        368 L    933 W      10701 Ch    "http://ghost.server:80/"                                                                                                         
000002020:   200        368 L    933 W      10701 Ch    "index.html"                                                                                                                      
000002145:   301        9 L      28 W       317 Ch      "javascript"                                                                                                                      
000000013:   403        9 L      28 W       277 Ch      ".htpasswd"                                                                                                                       
000000012:   403        9 L      28 W       277 Ch      ".htaccess"                                                                                                                       
000000011:   403        9 L      28 W       277 Ch      ".hta"                                                                                                                            
000003588:   200        510 L    1027 W     31535 Ch    "server-status"                                                                                                                   

Total time: 0
Processed Requests: 4614
Filtered Requests: 4607
Requests/sec.: 0

*stage 2 --> (light permutated extensions fuzzing wordlist:/usr/share/dirb/wordlists/common.txt)
********************************************************
* Wfuzz 3.1.0 - The Web Fuzzer                         *
********************************************************

Target: http://ghost.server:80/FUZZ.FUZ2Z
Total requests: 13842

=====================================================================
ID           Response   Lines    Word       Chars       Payload                                                                                                                           
=====================================================================

000000001:   403        9 L      28 W       277 Ch      "php"                                                                                                                             
000000031:   403        9 L      28 W       277 Ch      ".hta - php"                                                                                                                      
000000034:   403        9 L      28 W       277 Ch      ".htaccess - php"                                                                                                                 
000000032:   403        9 L      28 W       277 Ch      ".hta - html"                                                                                                                     
000000038:   403        9 L      28 W       277 Ch      ".htpasswd - html"                                                                                                                
000000002:   403        9 L      28 W       277 Ch      "html"                                                                                                                            
000000035:   403        9 L      28 W       277 Ch      ".htaccess - html"                                                                                                                
000000033:   403        9 L      28 W       277 Ch      ".hta - txt"                                                                                                                      
000000037:   403        9 L      28 W       277 Ch      ".htpasswd - php"                                                                                                                 
000000036:   403        9 L      28 W       277 Ch      ".htaccess - txt"                                                                                                                 
000000039:   403        9 L      28 W       277 Ch      ".htpasswd - txt"                                                                                                                 
000006050:   200        368 L    933 W      10701 Ch    "index - html"                                                                                                                    
000007039:   200        1 L      1 W        6 Ch        "login - php"                                                                                                                     

Total time: 0
Processed Requests: 13842
Filtered Requests: 13829
Requests/sec.: 0
```

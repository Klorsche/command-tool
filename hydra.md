# Hydra

Hydra is a parallelized login cracker which supports numerous protocols to attack. It is very fast and flexible, and new modules are easy to add. This tool makes it possible for researchers and security consultants to show how easy it would be to gain unauthorized access to a system remotely.

*basic syntax*
```
hydra -l USERNAME -P /path/to/wordlist TARGETIP [-t 4] PROTOCOL
```

*cracking User & Password*
```
hydra -L path/to/userlist -P /path/to/wordlist TARGETIP [-t 4] PROTOCOL
```

*specify different port*
```
hydra -s PORT -l USERNAME -P /path/to/wordlist TARGETIP [-t 4] PROTOCOL
```

*bruteforce a POST login form*
```
hydra -l USERNAME -P path/to/wordlist TARGETIP http-post-form "/LOGINPAGE:USERFIELDNAME=^USER^&PASSWORDFIELDNAME=^PASS^:LOGINFAILEDERRORMESSAGE"
```
  - Other protocols 
```
FTP, HTTP-FORM-GET, HTTP-FORM-POST, HTTP-GET, HTTP-HEAD, HTTP-PROXY, HTTPS-FORM-GET, HTTPS-FORM-POST, HTTPS-GET, HTTPS-HEAD, HTTP-Proxy, ICQ, IMAP, IRC, LDAP, MS-SQL, MYSQL, POP3, POSTGRES, RDP, SMTP, SMTP Enum, SNMP, SOCKS5, SSH (v1 and v2), Subversion, Telnet, VMware-Auth, VNC eXMP
```

# cURL

curl is a command line tool to transfer data to or from a server, using any of the supported protocols (HTTP, FTP, IMAP, POP3, SCP, SFTP, SMTP, TFTP, TELNET, LDAP or FILE). curl is powered by Libcurl. This tool is preferred for automation, since it is designed to work without user interaction. curl can transfer multiple file at once.

*Upload a file*
```
curl -T FILENAME SERVERADDRESS --user USERNAME:PASSWORD
```

*Download a file*
```
curl -u USERNAME:PASSWORD PROTOCOL://SERVERADDRESS -o FILENAME
```

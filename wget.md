# Wget

GNU Wget is a free software package for retrieving files using HTTP, HTTPS, FTP and FTPS, the most widely used Internet protocols. It is a non-interactive commandline tool, so it may easily be called from scripts, cron jobs, terminals without X-Windows support, etc. 

*Download a file from URL*
```
wget PROTOCOL://DOMAIN/FILE.EXT [-O RENAMEDFILE]
```

*Download a file who need User & Passwd*
```
wget PROTOCOL://USERNAME:PASSWD@DOMAIN/FILE.EXT
```
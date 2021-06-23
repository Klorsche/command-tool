# SSH

The Secure Shell Protocol (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network. Typical applications include remote command-line, login, and remote command execution, but any network service can be secured with SSH.

SSH provides a secure channel over an unsecured network by using a client–server architecture, connecting an SSH client application with an SSH server. The protocol specification distinguishes between two major versions, referred to as SSH-1 and SSH-2. The standard TCP port for SSH is 22. SSH is generally used to access Unix-like operating systems, but it can also be used on Microsoft Windows. Windows 10 uses OpenSSH as its default SSH client and SSH server.

*Basic Syntax*
```
ssh [OPTIONS] USER@TARGETIP [COMMAND]
```

*Example* 
```
ssh USER@TARGETIP [-p PORT]
```
```
ssh USER@TARGETIP [-p PORT] -i PRIVATEKEY.txt 
```

*Start ssh*
```
dpkg -l | grep ssh
```
* optional
```
sudo apt-get install openssh-server 
```
```
sudo systemctl enable ssh
```
```
sudo systemctl start ssh
```

*Edit ssh config file*
```
sudo vim /etc/ssh/sshd_config
```

*Data transfer from attacker to target*
```
scp FILENAME USER@TARGETIP:/path/to/destination [-i PRIVATEKEY.txt]
```

*Data transfer from target to attacker*
```
scp TARGETUSER@TARGETIP:/path/to/file path/where/you/want/to/save/file
```
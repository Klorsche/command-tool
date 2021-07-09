# User & Group

*User & Group enumeration*

current User
```
whoami
```

switch user
```
su USERNAME
```
	- su -l USERNAME (switch user & variables)

enumerate user privilege
```
sudo -l 
```

print user's group
```
groups
```

print active user
```
users
```
```
who
```
```
w
```

print last active sessions
```
last
```

*User & Group Management*

add, change and remove user 
```
useradd USERNAME
```
```
usermod USERNAME
```
```
userdel USERNAME
```

add, change and remove group 
```
groupadd GROUPNAME
```
```
groupmod GROUPNAME
```
```
groupdel GROUPNAME
```

change user password 
```
passwd USERNAME
```
remove user from group
```
gpasswd -d USERNAME GROUPNAME
```

*Permission*

change owner and group of file or directory
```
chown OWNER:GROUP FILENAME
```

change group owner of file or directory
```
chgrp GROUPNAME FILENAME
```

change permission on file or directory
```
chmod [0-7][0-7][0-7]
```
	- chmod -R (recorsive)
	- if you need to set SUID (e.g chmod 0777) (4 activate SUID; 2 activate SGID; 1 activate stickybit; 0 deactivate all)
	- chmod -x FILENAME (make file executable for everyone)

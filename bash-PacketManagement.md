# Packet Management

*File Zip*
```
zip ZIPARCHIVE.zip FILENAME
```
	- zip -e (zipping with password)

```
unzip ZIPARCHIVE.zip
```

*File Tar*
```
tar TARARCHIVE.tar FILENAME
```
	- tar -cfzv (archive and compress with gzip)
	- tar -xfzv (decompress tar archive)

*File GZip*
```
gzip -d FILE.gz
```

*DPKG*

Basic Syntax
```
dpkg OPTIONS PACKET
```

Key Switches 
```
-i (install packet)
-r (remove packet)
-l PACKETNAME (print installed packet)
-s (print packet status)
-S (find packet that contains a specified file)
```

*APT*

find packet that contains specific word
```
apt search WORD
```

find available software in repository APT
```
apt-cache search
```

print dependencies of a packet
```
apt-cache depends PACKETNAME
```

print info of a packet
```
apt-cache show
```
```
apt-cache showpkg
```

print list of upgradable packet
```
apt list --upgradable
```

update list of available packet
```
apt-get update
```

upgrade packet on the machine 
```
apt-get upgrade
```

upgrade packet on the machine and install most recent version and dependencies 
```
apt-get dist-upgrade -y
```

clear /var/cache/apt/archives or all file .deb 
```
apt-get clean
```
```
apt-get autoclean -y 
```

install packet
```
apt-get install PACKETNAME 
```

remove packet file (even configuration file)
```
apt-get --purge remove PACKETNAME
```

*OS Upgrade*
```
do-release-upgrade
```
	- need dist-upgrade first
	- do-release-upgrade -V (show version)
	- do-release-upgrade -f (GUI)
	- do-release-upgrade -c (print available new version)
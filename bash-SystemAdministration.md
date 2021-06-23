# System Administration

*Shutdown system*
```
shutdown
```
	- shutdown -h 0 (shutdown system immediately)

*Reboot system*
```
reboot
```

*Print system resources in realtime*
```
dstat
```

*Print actions from Kernel*
```
dmesg
```

*Print open descriptor in active processes*
```
lsof
```

*Print active processes*
```
ps -faux
```
	-f (tree)
	-a (all users)
	-u (process owner)
	-x (all processes)
	-j (print PPID)

*Print active process order by resources*
```
top
```

*Print process in background*
```
jobs -l 
```

*Bring background process in foreground*
```
fg %JOBNUMBER
```

*Push job in background*
```
bg %JOBNUMBER
```

*kill a process*
```
kill PID
```
	- kill -HUP PID  (close & reboot process)
	- kill -TERM PID (close process, clean context)
	- kill -KILL PID (terminate process)

# Netcat

*Basic Syntax*
```
nc [OPTIONS] HOST PORT
```

*Example*
```
nc -lvnp PORT
```
	- nc -l (listening)
	- nc -p (port)
	- nc -n (no DNS)
	- nc -v (verbose)

*UDP Connection*
```
nc -u HOST PORT
```

*Scan open ports*
```
nc -z HOST PORT-RANGE
```

*Data Transfer*

on the sender
```
nc RECIPIENTIP RECIPIENTPORT < FILENAME
```
on the recipient
```
nc -l RECIPIENTPORT > FILENAME
```

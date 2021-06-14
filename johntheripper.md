# John the Ripper

John the Ripper is designed to be both feature-rich and fast. It combines several cracking modes in one program and is fully configurable for your particular needs (you can even define a custom cracking mode using the built-in compiler supporting a subset of C). Also, John is available for several different platforms which enables you to use the same cracker everywhere (you can even continue a cracking session which you started on another platform).

*basic syntax*
```
john FILETOCRACK -w=path/to/wordlist
```

*show result in cleartext*
```
john --show path/to/file/hash-john
```

*how to crack password with etcpasswd and etcshadow*

```
copy the line we need from etcpasswd & etcshadow in a new file each
```
```
unshadow FILEPASSWD FILESHADOW > FILE4JOHN
```
```
john FILE4JOHN
```

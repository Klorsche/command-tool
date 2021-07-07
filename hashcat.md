# Hashcat

hashcat is the world’s fastest and most advanced password recovery utility, supporting five unique modes of attack for over 200 highly-optimized hashing algorithms. hashcat currently supports CPUs, GPUs, and other hardware accelerators on Linux, Windows, and OSX, and has facilities to help enable distributed password cracking.

*basic syntax*
```
hashcat -m HASHNUMBER -a METHOD FILETOCRACK [/path/to/wordlists/]
```

*Method* 
 - 0 - Dictionary Attack [need a wordlist]
 - 3 - Brute Force

HashNumber
https://hashcat.net/wiki/doku.php?id=example_hashes

*HashMask*
```
hashcat -m HASHNUMBER -a 3 FILETOCRACK [/path/to/wordlists/] ?l?l?l?l 
```
e.g. for a lowercase bruteforce of 4 digits

 ? | Charset
 
  - l  [abcdefghijklmnopqrstuvwxyz]
  - u  [ABCDEFGHIJKLMNOPQRSTUVWXYZ]
  - d  [0123456789]
  - s  [!"#$%&'()+,-./:;<=>?@[\]^]
  - a  [?l?u?d?s]
  - b  [0x00 - 0xff]

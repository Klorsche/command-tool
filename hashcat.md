#Hashcat

hashcat is the world’s fastest and most advanced password recovery utility, supporting five unique modes of attack for over 200 highly-optimized hashing algorithms. hashcat currently supports CPUs, GPUs, and other hardware accelerators on Linux, Windows, and OSX, and has facilities to help enable distributed password cracking.

*basic syntax*
,,,
hashcat -m Hashnumber -a Choosemethod filetocrack [/path/to/wordlists/]
,,,

+
Method 
0 - Dictionary Attack [need a wordlist]
3 - Brute Force

HashNumber
https://hashcat.net/wiki/doku.php?id=example_hashes
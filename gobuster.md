#GoBuster

Gobuster is a tool used to brute-force:

    - URIs (directories and files) in web sites.
    - DNS subdomains (with wildcard support).

Because I wanted:

    - something that didn’t have a fat Java GUI (console FTW).
    - to build something that just worked on the command line.
    - something that did not do recursive brute force.
    - something that allowed me to brute force folders and multiple extensions at once.
    - something that compiled to native on multiple platforms.
    - something that was faster than an interpreted script (such as Python).
    - something that didn’t require a runtime.
    - use something that was good with concurrency (hence Go).
    - to build something in Go that wasn’t totally useless.

*basic syntax*
,,,
gobuster dir -u TargetIP -w path/to/wordlist [-x php, sh, txt, cgi]
,,,
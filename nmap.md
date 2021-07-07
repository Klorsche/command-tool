# Nmap

Nmap (Network Mapper) is a free and open-source network scanner created by Gordon Lyon (also known by his pseudonym Fyodor Vaskovich). Nmap is used to discover hosts and services on a computer network by sending packets and analyzing the responses.

*basic syntax*

```
nmap [ScanType] [Options] TARGETIP
```

*Usage Example*
```
sudo nmap [-sS] -A -p- TARGETIP -oX filename.xml 
```
```
sudo nmap -sV -O TARGETIP -oX filename.xml
```

# Discovery Types

*SYN, ACK, UDP Discovery*
```
nmap -PS TARGETIP
```
This option sends an empty TCP packet with the SYN flag set. The default destination port is 80 (they are called "port 80 SYN probes"). Alternate ports can be specified as a parameter, for ex: 
-PS22-25,80,113,1050,35000.

The SYN flag suggests to the remote system that you are attempting to establish a connection. Normally the destination port will be closed, and a RST (reset) packet sent back. If the port happens to be open, the target will take the second step of a TCP three-way-handshake. Either the RST or SYN/ACK response 
tell Nmap that the host is available and responsive.

```
nmap -PA TARGETIP
```
The -PA option uses the same default port as the SYN probe (80) and can also take a list of destination ports in the same format (-PS22-25,80,113,1050,35000). The reason for offering both SYN and ACK ping probes is to maximize the chances of bypassing firewalls. 

It succeeds when -PS fails and vice versa. A solution to this problem is to send both SYN and ACK probes by specifying -PS and -PA

```
nmap -PU TARGETIP
```
Network exploration tool and security / port scanner -PU port list (UDP Ping). Another host discovery option is the UDP ping, which sends a UDP packet to the given ports. For most ports, the packet will be empty, though for a few a protocol-specific payload will be sent that is more likely to get a response.

The port list takes the same format as with the previously discussed -PS and -PA options. If no ports are specified, the default is 40125.

The primary advantage of this scan type is that it bypasses firewalls and filters that only screen TCP

*Arp ping*
```
nmap -PR TARGETIP
```

*Ping Scan*
```
sudo nmap -sn TARGETIP
```
It performs host discovery sending an ICMP echo request packet, a TCP SYN to port 443, a TCP ACK (if root, otherwise TCP SYN) to port 80 and an ICMP time stamp request packet, in order to verify if a host is available or not. 

*Host Listing*
```
nmap -sL TARGETIP
```
The list scan is a degenerate form of host discovery that simply lists each host of the network(s) specified, without sending any packets to the target hosts. By default, Nmap still does reverse-DNS resolution on the hosts to learn their names

# Scanning Type

*No-Discovery Scan*
```
nmap -Pn TARGETIP
```
```
nmap -P0 TARGETIP
```
Pn - The key concept here is that if discovery fails for a particular host, Nmap doesn’t scan it. This means you have to ensure that the options you give to Nmap will find hosts in the discovery phase. 

P0 - basically says to Nmap, “Don’t worry about discovery — just scan.” 

It would let a tester scan every TCP port from a network that is blocking ICMP with fingerprinting and service detection. It marks all hosts as "online" by default.

*Stealth Scan - Root Default*
```
sudo nmap [-sS] TARGETIP
```
SYN scanning is a TCP port scanning method that involves sending SYN packets to various ports on a target machine without completing a TCP handshake. If discovery fails, it doesn't perform any scan

*TCP Scan - Without Root Default*
```
nmap [-sT] TARGETIP
```
When a user running nmap does not have raw socket privileges, Nmap will default to the TCP connect scan. Because Nmap has to wait for the connection to complete before the API will return the status of the connection, a connect scan takes much longer to complete than a SYN scan. TCP connect scan is the default TCP scan type when SYN scan is not an option. Not only TCP connect scan takes longer and require more packets to obtain the same information, but target machines are more likely to log the connection. It is the most reliable, but also visible.

*TCP ACK Scan*
```
nmap -sA TARGETIP
```
Used to map Firewall Ruleset (statefull, stateless, ports filtered)

*UDP Scan*
```
sudo nmap -sU TARGETIP
```
The UDP scan (-sU) can also be used in conjunction with a TCP SYN scan (-sS) option to build a more complete picture of our target

*Operating System Scan*
```
sudo nmap -O TARGETIP
```
This feature attempts to guess the target’s operating system (OS) by inspecting returned packets. This is possible because operating systems often have slightly different implementations of the TCP/IP stack.

*Version Scan*
```
nmap -sV  [ --version-intensity (0-9) ] TARGETIP
```
We can also identify services running on specific ports by inspecting service banners (-sV) and running various OS and service enumeration scripts (-A) against the target (-A can be used for the same purpose with further information). 

Keep in mind that banners can be modified by system administrators. As such, these can be intentionally set to fake service names in order to mislead a potential attacker. Banner grabbing has a significant impact on the amount of traffic used as well as the speed of the scan

*Protocol Scan*
```
sudo nmap -sO TARGETIP
```
IP protocol scan determines which protocols are supported on target machine (ICMP, TCP, IGMP, etc.). It returns protocol, state and service.
IP protocol scan allows you to determine which IP protocols (TCP, ICMP, IGMP, etc.) are supported by target machines. This isn´t technically a port scan, since it cycles through IP protocol numbers rather than TCP or UDP port numbers.

*Aggressive Mode Scan*
```
nmap -A TARGETIP
```
Sometimes the results we're getting just aren't enough. If we don't care about how loud we are, we can enable "aggressive" mode. This is a shorthand switch that activates service detection, operating system detection, a traceroute and common script scanning.


The point is to enable a comprehensive set of scan options without people having to remember a large set of flags. This enables OS detection (-O), version scanning (-sV), script scanning (-sC) and traceroute (--traceroute). This option only enables features, and not timing options (such as -T4).

Determines the application name and version number where available—not just the service protocol. Supports both the TCP and UDP protocols, multi-platform. Enables OS detection, version detection, script scanning, and traceroute.


# Ports & Timing Options

*Specific Ports*
```
nmap [ScanType] -p [(Port,Number) or (-) ALLPORTS] TARGETIP
```

*Open Ports, Top Ports, Exclude Host*
```
nmap [ScanType] --open --top-ports [NUMBERPORTS] TARGETIP/CIDR --exclude IP,to,exclude
```

*Fast Scan - only 100 ports*
```
nmap [ScanType] -F TARGETIP
```

*Timing Options*
```
nmap [ScanType] -T (0-1-2-3-4-5) TARGETIP
```
The first two are for IDS evasion. Polite mode slows down the scan to use less bandwidth and target machine resources. Normal mode is the default and so -T3 does nothing. Aggressive mode speeds scans up by making the assumption that you are on a reasonably fast and reliable network. Finally insane mode assumes that you are on an extraordinarily fast network or are willing to sacrifice some accuracy for speed.  -T4 is recommended.


# Output Format

*Greppable Format*
```
nmap [ScanType] TARGETIP -oG filename.txt
```

*XML Format*
```
nmap [ScanType] TARGETIP -oX filename.xml 
```

*All available Format*
```
nmap [ScanType] TARGETIP -oA filename.xml 
```

# Other Switches

```
-v (Verbose)
-R  (Do reverse-DNS resolution)
-n	(Never do DNS resolution)
-iL (take input from list)
--reason/--packet-trace (describe which discovery test host responds/more details option)
-sN (Null Scan -  Does not set any bits TCP flag header is 0)
-sF (FIN Scan - Sets just the TCP FIN bit)
-sX (Xmas Scan - URG, PUSH and FIN flags are set. It helped avoid some type of low-level firewall. Advanced firewall block this scan)
-f (used to fragment the packets making it less likely that the packets will be detected by a firewall or IDS)
--scan-delay (used to add a delay between packets sent. This is very useful if the network is unstable, but also for evading any time-based firewall/IDS triggers which may be in place)
--badsum (this is used to generate in invalid checksum for packets. Any real TCP/IP stack would drop this packet, however, firewalls may potentially respond automatically, without bothering to check the checksum of the packet. As such, this switch can be used to determine the presence of a firewall/IDS)
```

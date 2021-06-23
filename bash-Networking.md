# Networking

*Show hostname*
```
hostname
```
	- hostname -f (show FDQN)
	- hostname -d (print target domain)
	- hostname -I (print target IP)

*Ping IP*
```
ping IP/HOSTNAME
```
	- ping -t (continuous ping)
	- ping -a (resolve IP to hostname)
	- ping -6 (force use of IPV6)
	- ping -4 (force use of IPV4)
	- ping -i (set time to live)
	- ping -n (set number of packet)

*Show domain information*
```
whois DOMAINNAME
```

*Show active connection*

Example
```
sudo ss -tulw
```
```
sudo ss -tulwn
```
```
sudo ss -tulpn
```
	- t = tcp
	- u = udp
	- l = listening socket
	- p = list process name that opened sockets
	- n = don't resolve service name

*Show packets routing*
```
traceroute IP/HOSTNAME
```
	- tracepath (show single hop response time)
	- mtr (GUI & monitoring)

*Show IP*
```
ip addr
```

*Show ARP Table*
```
ip neigh show
```
	- also "ip neighbour" or "ip neighbor"
	- ip neigh add {IP} lladdr {MAC/LLADDRESS} dev {DEVICE} [nud {STATE}]  (add record to ARP table)
	- ip neigh del {IP} dev {DEVICE}  (delete ARP record)
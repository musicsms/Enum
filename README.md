# Enum

Scan with Nmap:
```
nmap -sV -O --top-ports 50 --open -oA nmap/initial <ip or cidr>
nmap -sC -sV -O --open -p- -oA nmap/full <ip or cidr>
nmap -sU -p- -oA nmap/udp <ip or cidr>

--top-ports only scan the N most common ports
--open only show open ports
-sC use the default scripts
-sV detect versions
-O detect Operating Systems
-p- scan all the ports
-oA save the output in normal format, grepable and xml
-sU scan UDP ports
```
Is also possible to specify scripts or ports:
```
nmap --scripts vuln,safe,discovery -p 443,80 <ip or cidr>
```
If there are servers that could be not answering (ping), then add the flag -Pn (example of initial one):
```
nmap -Pn --top-ports 50 --open -oA nmap/initial <ip or cidr>
```
Most uses:
```
nmap -T4 -A -p1-65355 <ip>
```


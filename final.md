### Convert numbers:

```echo "obase=2; <decimal>" | bc =======> 45 -> 101101```
```echo "ibase=1; <binary>" | bc ======> 101101 -> 45```

### Iptables:

Just use man dude

```sudo iptablesd -I INPUT -p tcp --dport 990 -s 127.0.0.1 -j ACCEPT```
*just to be sure

### Find ports:

```sudo nmap localhost -p <ports-range>```

### Ports config:

config file: ```sudo systemctl edit ssh.socket``` -> 

[Socket]
ListenStream=22

```sudo systemctl demon-reload```

```sudo systemctl restart ssh.socket```

### User config:

```sudo adduser <name>```

```sudo vim /etc/ssh/sshd_config```

-> 

PasswordAuthentication yes
KbdInteractiveAuthentication yes

-> 

```sudo systemctl restart ssh```


### Find service:

```nslookup <service> (like kse.ua)```

### Traceroutes

```traceroute -m 5 kse.ua```

### Calculate network

```sudo apt install ipcalc```

```ipcalc 10.0.0.1/23```

### Find command

```sudo find <dir> -type f -name "<name>"```

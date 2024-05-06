# 4.Execution_of_NetworkCommands
## NAME : DHARANISH MS
## REGISTER NO : 212223240027

# AIM :Use of Network commands in Real Time environment
# Software : Command Prompt And Network Protocol Analyzer
# Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.

# PROGRAM
## CLIENT
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## SERVER
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
## TRACEROUTE COMMAND
```
from scapy.all import*     
target = ["www.google.com"]     
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
# Output
## CLIENT
![CLIENT 4](https://github.com/MSDharanish-23011819/4.Execution_of_NetworkCommends/assets/147139454/306ea4fc-d1fe-44a7-89cd-434ef18c6c6a)

## SERVER
![SERVER 4](https://github.com/MSDharanish-23011819/4.Execution_of_NetworkCommends/assets/147139454/dea572c4-6ca6-4717-bba3-4852257883dd)

## TRACEROUTE COMMAND
![TRACE 4](https://github.com/MSDharanish-23011819/4.Execution_of_NetworkCommends/assets/147139454/c2f3e985-7723-4eff-bf71-918c72e9a98f)

# Result
Thus Execution of Network commands Performed. 

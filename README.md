# 4.Execution_of_NetworkCommands
## NAME : dhanussh elango
## REG NO : 212224040069
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
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
<BR>

## Program
```
SERVER
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

CLIENT

import socket
s=socket.socket()
s.connect(('localhost',8000)) 
while True:
  ip=input("Enter the website you want to ping ")
  s.send(ip.encode()) print(s.recv(1024).decode())
```



## OUTPUT
# netstat
<img width="1241" height="1090" alt="image" src="https://github.com/user-attachments/assets/f57978ca-17bb-415d-82ad-92e148c65f92" />

# ipconfig
<img width="1118" height="831" alt="image" src="https://github.com/user-attachments/assets/9016e5b8-be3c-40a8-90e0-2a5f0e2d8ebc" />

# ping
<img width="1124" height="555" alt="image" src="https://github.com/user-attachments/assets/159367b0-fe7c-4ac8-88ae-8bf7845e97cc" />

# tracert
<img width="1140" height="684" alt="image" src="https://github.com/user-attachments/assets/33b78a2f-e7ea-4372-8cec-ba8aa2f4bab9" />

# nslookup
<img width="1146" height="597" alt="image" src="https://github.com/user-attachments/assets/7da79808-cca2-4328-a3dc-19223a69f427" />

# getmac
<img width="1193" height="275" alt="image" src="https://github.com/user-attachments/assets/3d2937d3-c74b-4d50-a0c4-329c373cfa94" />

# hostname
<img width="1163" height="206" alt="image" src="https://github.com/user-attachments/assets/dd591041-7ed8-4af4-b504-a2708cd009a4" />


## OUTPUT




## Result
Thus Execution of Network commands Performed 

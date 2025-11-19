# 4.Execution_of_NetworkCommands
## NAME : VENKATESAN R
## REG NO : 212224230299
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
<img width="425" height="273" alt="image" src="https://github.com/user-attachments/assets/d2800253-b8eb-470a-a065-1ed9d9b870fc" />

# ipconfig
<img width="680" height="727" alt="image" src="https://github.com/user-attachments/assets/b3cb5622-5514-407e-931b-5cb69d273d6f" />

# ping
<img width="594" height="197" alt="image" src="https://github.com/user-attachments/assets/680fd29a-4ecf-48bf-96e3-1ed0f3146867" />

# tracert
<img width="1071" height="483" alt="image" src="https://github.com/user-attachments/assets/1b95ae7f-e159-470f-a169-93a362b8317f" />

# nslookup
<img width="614" height="493" alt="image" src="https://github.com/user-attachments/assets/1c8f2b55-959f-46a1-8436-46d0df88f04f" />

# getmac
<img width="977" height="219" alt="image" src="https://github.com/user-attachments/assets/e3c89606-d4f9-409e-a2be-4d811dad7945" />

# hostname
<img width="376" height="70" alt="image" src="https://github.com/user-attachments/assets/e47ad72a-f01f-4b5f-ad51-bc9c1ff61533" />


## OUTPUT

<img width="920" height="195" alt="image" src="https://github.com/user-attachments/assets/c5fbcd2a-2ce5-47c6-98db-44d389987c48" />



## Result
Thus Execution of Network commands Performed 

# 4.Execution_of_NetworkCommands
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


## Output
server:

```
# server.py
import socket

# Server configuration
host = '127.0.0.1'  # localhost
port = 5000         # port number

# Create TCP socket
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server_socket.bind((host, port))
server_socket.listen(1)
print(f"Server listening on {host}:{port}")

# Accept client connection
conn, addr = server_socket.accept()
print(f"Connected by {addr}")

while True:
    data = conn.recv(1024).decode()
    if not data:
        break
    print(f"Received from client: {data}")
    conn.send(f"Server received: {data}".encode())

conn.close()
server_socket.close()
```
client:
```
# client.py
import socket

# Server configuration
host = '127.0.0.1'  # localhost
port = 5000

# Create TCP socket
client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client_socket.connect((host, port))

while True:
    message = input("Enter message to send (type 'exit' to quit): ")
    client_socket.send(message.encode())
    if message.lower() == 'exit':
        break
    data = client_socket.recv(1024).decode()
    print(f"Received from server: {data}")

client_socket.close()
```
##output
<img width="1919" height="1199" alt="Screenshot 2025-11-14 090758" src="https://github.com/user-attachments/assets/9aa16c88-b2c5-4d17-82d8-9e0d7277005f" />


## Result
Thus Execution of Network commands Performed 

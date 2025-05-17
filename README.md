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

## program
client
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
       
server
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```


## Output
PING
![Screenshot 2025-05-17 131520](https://github.com/user-attachments/assets/879b3f2c-4aa1-4ca0-8948-70dad9fa8005)

![Screenshot 2025-05-17 131533](https://github.com/user-attachments/assets/c9e5243a-822c-4888-8311-e75b201ca007)

TRACERT

![Screenshot 2025-05-17 133509](https://github.com/user-attachments/assets/bcd2cc86-6a8c-4213-ab91-457937aab65b)

IPCONFIG

![Screenshot 2025-05-17 133558](https://github.com/user-attachments/assets/4d3bf1bb-76ba-4619-8d9d-bdaa9d55dd6c)

NBTSTAT

![Screenshot 2025-05-17 134143](https://github.com/user-attachments/assets/63e5a5dc-33ab-468d-b065-cc38907ca265)

NSLOOKUP

![Screenshot 2025-05-17 133752](https://github.com/user-attachments/assets/3308554c-866b-46de-a296-24474efca719)

HOSTNAME

![Screenshot 2025-05-17 133903](https://github.com/user-attachments/assets/18ecbdbb-efcf-4774-8436-df4062bff703)

NETSTAT

![Screenshot 2025-05-17 133937](https://github.com/user-attachments/assets/f33609ec-f769-4706-82a1-1bf927917d97)

GETMAC

![Screenshot 2025-05-17 133957](https://github.com/user-attachments/assets/f082cd05-8ab5-42ea-8dac-9374d9aaf69d)


## Result
Thus Execution of Network commands Performed 

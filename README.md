# EX-6 IMPLEMENTATION OF PING COMMAND

### DATE :12-04-2023

### AIM :
To write the python program for simulating ping command

### ALGORITHM :
1. start the program.
2. Include necessary package in java.
3. To create a process object p to implement the ping command.
4. declare one Buffered Reader stream class object.
5. Get the details of the server
6. length of the IP address.
7. time required to get the details.
8. send packets, receive packets and lost packets.
9. minimum, maximum and average times.
10. print the results.
11. Stop the program.

### PROGRAM :
### Client:
```
# Developed by : Gowrisankar.p
# Register Number : 212222230041
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
### Server:
```
# Developed by : S.JAIGANESH
# Register Number : 212222240037
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```
### OUTPUT :
### Client:
![image](https://github.com/gowrisankarponnusamy/EX-6/assets/119393123/8bb6a525-5550-4db3-b4cc-df8b048937e3)

### Server:
![image](https://github.com/gowrisankarponnusamy/EX-6/assets/119393123/3d98dbd7-0ccb-43f4-a92a-4d6d0c385cfd)

### RESULT :
Thus, the python program for simulating ping command was successfully executed.


# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
TARANIKKA A
212223220115
B TECH (IT)
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
 ```
import socket
 HOST = '127.0.0.1'  
 PORT = 65432       
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
s.bind((HOST, PORT))
 s.listen()
 conn, addr = s.accept()
 with conn:
 print('Connected by', addr)
 while True:
 data = conn.recv(1024)
 if not data:
  break
 conn.sendall(data) 
 ```
## SERVER
```
 import socket
 HOST = '127.0.0.1' 
 PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
 s.connect((HOST, PORT))
 while True:
 message = input("Enter message to send to server: ")
 ```
## OUPUT
## CLIENT
![image](https://github.com/aswethaashok/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149987410/b046236e-91e9-430a-985c-8ca414f4a370)

## SERVER 
![image](https://github.com/aswethaashok/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149987410/2d30f721-c2ee-4670-86e7-3890489a8212)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

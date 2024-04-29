# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Client
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```

### Server
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT:
### Client
![image](https://github.com/Loknaath-sec/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742558/c83f7de0-a30f-45fa-891b-c5859108e564)
### Server
![image](https://github.com/Loknaath-sec/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742558/80ca15ba-c7a1-48d2-9a3a-48f9c3e22c7c)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

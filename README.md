# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUPUT
## Client:
![WhatsApp Image 2024-05-10 at 10 59 57_032d6205](https://github.com/srrihaari/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145550674/234e41fa-7f86-45a0-95de-29850b3ca210)

## Server:
![WhatsApp Image 2024-05-10 at 11 00 00_779940e5](https://github.com/srrihaari/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145550674/890cee03-6d2e-4454-9f0b-f61435aca57d)


## RESULT:

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

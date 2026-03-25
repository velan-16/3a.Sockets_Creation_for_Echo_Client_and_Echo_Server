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
server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
<img width="1919" height="1019" alt="562033636-9a1cf2d4-b555-466c-b487-ec5ea4ecf360" src="https://github.com/user-attachments/assets/3e165e0c-1de3-43b6-b50a-84b82807501b" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## server.py
```
import socket
s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)
print("Waiting for connection...")
c, addr = s.accept()
print("Connected to:", addr)
while True:
    ClientMessage = c.recv(1024).decode()
    print("Client >", ClientMessage)
    msg = input("Server > ")
    c.send(msg.encode())
```
## client.py
```
import socket
s = socket.socket()
s.connect(('localhost', 8000))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server >", s.recv(1024).decode())
```
## OUTPUT

<img width="1898" height="305" alt="image" src="https://github.com/user-attachments/assets/b2d472d2-d4ad-4457-999b-b5e9e68277c5" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

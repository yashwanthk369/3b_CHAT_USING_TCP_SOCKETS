# 3b.CREATION FOR CHAT USING TCP SOCKETS

# Name : Yashwanth K

# Reg No : 212224040369

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

server.py

```
import socket

s = socket.socket()
s.bind(('localhost', 8001))
s.listen(5)

c, addr = s.accept()

while True:
    ClientMessage = c.recv(1024).decode()
    print("Client > ", ClientMessage)
    msg = input("Server > ")
    c.send(msg.encode())
```

client.py

```
import socket

s = socket.socket()
s.connect(('localhost', 8001))

while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
```
## OUTPUT

## server.py

<img width="1063" height="162" alt="image" src="https://github.com/user-attachments/assets/cd294a2e-9b4d-4a65-bc1d-4becc8792f56" />

## client.py

<img width="1064" height="190" alt="image" src="https://github.com/user-attachments/assets/90ea0dde-e433-454d-a11e-0d16990c2378" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

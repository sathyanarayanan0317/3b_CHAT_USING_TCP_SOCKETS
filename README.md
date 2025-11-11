# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME : SATHYANARAYANAN M
### REGISTER NO : 212224040300
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
### CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

## OUTPUT
<img width="1911" height="1115" alt="Screenshot 2025-10-22 103621" src="https://github.com/user-attachments/assets/2fc79f65-2e01-452a-a8bd-b6eaf559adbd" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

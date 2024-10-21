# 3B CREATION FOR CHAT USING TCP SOCKETS

## AIM
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
5. 
## PROGRAM

## Client 
```import socket
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
## Server
```s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

## OUPUT
![Screenshot 2024-10-21 161513](https://github.com/user-attachments/assets/66ff103d-794e-41d1-95a9-51028ceb067f)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

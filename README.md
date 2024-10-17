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
# client :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
# server:
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
## OUPUT:
client:
![3bclient](https://github.com/Prasanavausdevan/3b_CHAT_USING_TCP_SOCKETS/assets/144870579/1c0d469d-5779-465a-904c-24a6e04c9963)


server:

![3bserver](https://github.com/Prasanavausdevan/3b_CHAT_USING_TCP_SOCKETS/assets/144870579/39b048b9-d353-4a6e-b84c-5322edc700af)T
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME: K KESAVA SAI
## REGISTER NUMBER: 212223230105
## AIM:
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```PY
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```

## SERVER:
```PY
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
## Client:
![image](https://github.com/user-attachments/assets/ad6c7d72-4bba-4908-8cce-10a31d9d8e96)
## Server:
![image](https://github.com/user-attachments/assets/164ecad4-ab38-4e97-b0e4-4f545b85ccf5)

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

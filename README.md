# APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## EXP: 9

## DATE: 03-05-2023

# AIM:
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM:
# Client:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
server
4. Send and receive the message using the send function in socket.
# PROGRAM:
# CLIENT:
```python3
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
  ```
# SERVER:
```python3
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
   
# CLIENT OUTPUT : 

![client9](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/EX-9/assets/119559905/fff0a81d-2f8f-4a4d-a0a4-6c657895216f)


# SERVER OUTPUT :

![server9](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/EX-9/assets/119559905/5e941853-2dd3-4014-9caa-fe5429d5d588)


# RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully
created and executed.

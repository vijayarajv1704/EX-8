# APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER



# EXP: 8

# DATE:26-04-2023

# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

# ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
server.
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
   c.send(ClientMessage.encode())
```
   
# CLIENT OUTPUT : 
![image](https://github.com/SudharsanamRK/EX-8/assets/115523484/d7dd9d06-1e79-4bca-b7dc-d3dc7daabece)

# SERVER OUTPUT :
![image](https://github.com/SudharsanamRK/EX-8/assets/115523484/b08b7e8a-5f67-4a15-bafa-63b05e9d14e5)


# RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links
was successfully created and executed.

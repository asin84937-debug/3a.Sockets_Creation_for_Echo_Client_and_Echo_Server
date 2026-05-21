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
## Client.py:
```
import socket 
s=socket.socket() 
s.connect(('localhost',9000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## Server.py:
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## OUPUT
## Client.py:
<img width="555" height="710" alt="Screenshot 2026-05-21 143800" src="https://github.com/user-attachments/assets/4339feae-9096-486d-a8c3-b204323fbbe0" />
## Server.py:
<img width="578" height="807" alt="Screenshot 2026-05-21 143821" src="https://github.com/user-attachments/assets/4e95e7b0-3bae-4403-baa9-f593842e8f2b" />

## Developed by : A.Asin banu
## Register no : 212225040035
## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

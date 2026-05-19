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
## server.py
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

## OUPUT
client:
<img width="679" height="301" alt="Screenshot 2026-05-19 140233" src="https://github.com/user-attachments/assets/6ac755fc-22e4-49e1-90f5-466d7ab18919" />

server:
<img width="690" height="445" alt="Screenshot 2026-05-19 140226" src="https://github.com/user-attachments/assets/0f14d69c-9cb0-44ab-bd4f-d33596a059b3" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

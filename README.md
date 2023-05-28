# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE :

## AIM :
       
       To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM :
           
           1. Start the program.
           2. Get the frame size from the user
           3. To create the frame based on the user request.
           4. To send frames to server from the client side.
           5. If your frames reach the server, it will send ACK signal to client otherwise it will send NACK signal to client.
           6. Stop the program

## PROGRAM :
```
Developed by JANANI.S
Register Number:212222230049

CLIENT:

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
    
SERVER:

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
````
## OUTPUT :

CLIENT:

![5client](https://github.com/JananiSoundararajan/EX-8/assets/119477549/d036597c-5af4-4632-b286-d30566db334d)

SERVER:

![5server](https://github.com/JananiSoundararajan/EX-8/assets/119477549/2695cd31-2b50-4c70-b44c-6daa7061e31b)

## RESULT :

      Thus,the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.

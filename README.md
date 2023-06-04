# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE : 27-04-2023

AIM :

 To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

ALGORITHM :

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it will
send NACKsignal to client.
6. Stop the program

PROGRAM :

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode()) 
```

SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```

CLIENT OUTPUT :

![EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT](https://github.com/Jeevapriya14/EX-8/assets/121003043/ea1bc0ce-1be3-4773-b4e3-840f17ce3ffb)

SERVER CLIENT:

![EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO SERVER](https://github.com/Jeevapriya14/EX-8/assets/121003043/5ada2785-74f5-4521-976b-357d3f607bea)


RESULT :

 Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.

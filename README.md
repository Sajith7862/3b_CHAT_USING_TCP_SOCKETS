# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME : MOHAMED HAMEEM SAJITH J
## REG NO : 212223240090
## AIM  :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
   
## PROGRAM :

### CLIENT :

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### SERVER :

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

## OUTPUT :

### CLIENT :

![image](https://github.com/user-attachments/assets/e783dc1c-de61-4039-b0ef-0a9d7663b055)

### SERVER :

![image](https://github.com/user-attachments/assets/386a33b3-a2b8-4283-a4ec-b0f16e8e987d)

## RESULT :

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

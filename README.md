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
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
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
![image](https://github.com/23000966/3b_CHAT_USING_TCP_SOCKETS/assets/153983364/05f06534-d292-4dd2-b531-460b9ff69914)
![image](https://github.com/23000966/3b_CHAT_USING_TCP_SOCKETS/assets/153983364/0fc282a3-0c2c-4a34-9231-c5cf1b904e74)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

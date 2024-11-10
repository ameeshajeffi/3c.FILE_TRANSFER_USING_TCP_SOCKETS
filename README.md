# 3c.CREATION FOR FILE TRANSFER USING TCP SOCKETS
## AIM
To write a python program for creating File Transfer using TCP Sockets Links
## ALGORITHM:
1. Import the necessary python modules.
2. Create a socket connection using socket module.
3. Send the message to write into the file to the client file.
4. Open the file and then send it to the client in byte format.
5. In the client side receive the file from server and then write the content into it.
## PROGRAM
### SERVER:
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
## OUTPUT:
### SERVER : 
![image](https://github.com/arbasil05/3b_CHAT_USING_TCP_SOCKETS/assets/144218037/7a1db6d1-2a7a-4cd7-8464-dea2b8450bcf)

### CLIENT: 
![image](https://github.com/arbasil05/3b_CHAT_USING_TCP_SOCKETS/assets/144218037/735b233f-ddde-4d1a-acce-b48f78f5ea2c)


## RESULT
Thus, the python program for creating File Transfer using TCP Sockets Links was 
successfully created and executed.

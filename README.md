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
## Client:

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

## Server:

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())


## OUPUT
## Client:
![WhatsApp Image 2024-05-10 at 10 59 57_5a417102](https://github.com/cherryscharan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/146930617/a26f044a-31af-4784-b904-a688ba16bf94)

## Server:
![WhatsApp Image 2024-05-10 at 11 00 00_52c8f85f](https://github.com/cherryscharan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/146930617/480c4064-9f84-42ad-8d3c-6e1c7b9b70d3)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

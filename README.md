# 2a_Stop_and_Wait_Protocol
## Name: Mugil Raj S A
## Register No:212223220062
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break

```
SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())

```
## OUTPUT
CLIENT:

![Screenshot 2024-05-14 172650](https://github.com/MugilRaj1105/2a_Stop_and_Wait_Protocol/assets/154905390/08569e1d-94f1-4ca5-8b4d-031437234c5a)

SERVER:

![Screenshot 2024-05-14 172711](https://github.com/MugilRaj1105/2a_Stop_and_Wait_Protocol/assets/154905390/61b58ad0-9d1a-4035-b97b-9b64fbf53351)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.# 2a_Stop_and_Wait_Protocol

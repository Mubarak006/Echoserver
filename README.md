# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
server:

import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST,PORT)) as s:
    conn,addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)

client:
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Mubarak R, 212224220066')
    print(f'Received: {s.recv(1024)!r}')
```


## OUTPUT:
:![EH EX1](https://github.com/user-attachments/assets/1bdfb926-1b6d-4301-ae7e-f93357ae27ad)

## RESULT:

The program is executed successfully

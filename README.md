# Encrypted-Chat-Server-IN-C
Establish a encrypted connection between client and server in C using OpenSSL

First Of All Install OpenSSL

OpenSSL Guide: https://help.ubuntu.com/community/OpenSSL

Now Create A Certificate File "mycert.pem" the Name of the certificate:

Command Line : openssl req -x509 -nodes -days 365 -newkey rsa:1024 -keyout mycert.pem -out mycert.pem

Compile Server:

Command Line : gcc -Wall -o ssl-server ssl-server.c -L/usr/lib -lssl -lcrypto

Run Server : 
Command Line : sudo ./ssl-server <portnum> || Ex: sudo ./ssl-server 6000

Compile Client :
Command Line : gcc -Wall -o ssl-client ssl-client.c -L/usr/lib -lssl -lcrypto

Run Client :
Command Line : ./ssl-client <IP> <portnum> || ./ssl-client 192.168.43.54 6000




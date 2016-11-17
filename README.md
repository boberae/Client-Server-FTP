# Client-Server-FTP

Multi-threaded FTP server can handle multiple clients simultaneously

FTP Commands available to client:

1. CONNECT <server name/IP address> <server port>: This command allows a
client to connect to a server. The arguments are the name/IP address of the
server – for instance cis.gvsu.edu – and the port number on which the server
is listening for connections. Once the control connection is established, a data
connection with the server has to be setup for each data transaction operation
(You can have this part hard-coded in the client and server code).

2. LIST: When this command is sent to the server, the server returns a list of the
files in the current directory on which it is executing. The client should get the
list and display it on the screen.

3. RETR <filename>: This command allows a client to get a file specified by its
filename from the server.

4. STOR <filename>: This command allows a client to send a file specified by its
filename to the server.

5. QUIT: This command allows a client to terminate the control connection. On
receiving this command, the client should send it to the server and terminate
the connection. When the ftp_server receives the quit command it should
close its end of the connection.

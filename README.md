# MarsNATRP
Release: https://github.com/SmartGhost0/MarsNATRP/releases

How To Use
-----

* You should download the release files or project.The release pack include MarsNATRP_Server and MarsNATRP_Client.This application was written by .netCore which is easy to make the application run on muti-platform. If you do not find the files which can run on your platform,you can just use the portable vision(.netCore Framework is required).

Run Application
-----
   *MarsNATRP_Client
         Windows:Run MarsNATRP_Client.exe {ServerIP} {ServerPrivatePort} {LocalIP} {LocalPort}
         Linux/Unix:Run MarsNATRP_Client {ServerIP} {ServerPrivatePort} {LocalIP} {LocalPort}
         For example: If you want to map the private port 8888 of public address 10.10.10.10 to the port 80 of local address 127.0.0.1 you should run MarsNATRP_Client like this.
         Win:MarsNATRP_Client.exe 10.10.10.10 8888 127.0.0.1 80
         L/U:MarsNATRP_Client 10.10.10.10 8888 127.0.0.1 80
   *MarsNATRP_Server
         Windows:Run MarsNATRP_Server.exe {ServerIP} {ServerPublicPort} {ServerIP} {ServerPrivatePort}
         Linux/Unix:Run MarsNATRP_Server {ServerIP} {ServerPublicPort} {ServerIP} {ServerPrivatePort}
         For example: If you want to map the public port 8080 of public address 10.10.10.10 to the port 8888 of address 10.10.10.10 you should run MarsNATRP_Client like this.
         Win:MarsNATRP_Client.exe 10.10.10.10 8080 10.10.10.10 8888
         L/U:MarsNATRP_Client 10.10.10.10 8080 10.10.10.10 8888
         
Test
-----
   *Test Application
      Try to start a website on local IP:Port and Try to visit PublicIP:Port
         for example: if you run applicaion like the example of "Run Application",you should run website on 127.0.0.1:80 and visit the public server 10.10.10.10:8080
            *How does it works 
               When user connect to 10.10.10.10:8080 the server will listen 10.10.10.10:8888 to accept the connection of client when the client connected the client will connect to 127.0.0.1:80.After this the reverse proxy bridge can create successful.

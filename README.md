# Paxos-Implementaion
This project implements Paxos algorithm using C#


Important Notes

1) The makefile uses "mcs" to compile the C sharp code and is specific to Mono tool. The Mono tool needs to be setup.

2) Cygwin terminal is required to be used for executing the makefile in a Windows machine. STEP #3 IS NOT RELEVANT FOR LINUX MACHINE

3) Execute the makefile provided in the bundle to compile the code for each node. The bundle includes both the server and the client application.

5) During the execution of the process, below are the files that are created. Please note that each of this file is created in the same folder location as the executable(the executable shall be created in the same location as the project folder). a) KeyValue file - To store the key and the values entered using the PUT process. b) Log File - To store the server loggings. c) ClientLog File - To store the client loggings.

Components

Client: This is the Source Code for Client Application.
RemoteServer: Solution Folder has two projects: TCP Server Application and UDP Server Application
TwoPhaseServer: This class library is called remotely from the client via HTTP and it internally uses "RemoteMethods" to do the core operations. This library also has the definition to communicate to other peer servers.
RemoteMethods: Class library that has definition of the three core operations(GET, PUT, Delete).
Makefile

How to run

ADD the Server names (along with port numbers) in the APP.CONFIG on the "RemoteServer" and "Client".

The first server IP and PORT NUMBER should be of the leader

Server: Run the executable from the command prompt by passing the port number as the parameter. The port number should be same as the one in App.config files.

Client: Run the executable from the command prompt (Client.exe). Client is an interactive console application.

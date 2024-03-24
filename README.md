# PeerToPeerTerminal
# Secure Peer-to-Peer Terminal Application

In this socket programming assignment, we will be implementing a secure peer-to-peer terminal emulation application using C programming language, using server as intermediate and with a secure communication using SSL encryption. Controller client will be accessing the remote client to run terminal commands. This project aims to provide a secure and efficient means of remote command execution. To address the challenges presented by NAT and firewalls, the project will incorporate a relay server as intermediary. This server will play a vital role in facilitating authentication and communication between the controller client and the remote client, overcoming network obstacles and ensuring a reliable connection. This approach aligns with the goal of providing a secure alternative to traditional remote screen sharing, particularly suited for scenarios with slower bandwidth or heightened security requirements. 
Remote client should be started first and connect to the server with a specific session ID chosen by user. The server stores the details of the new remote client in its database. Then, the controller client will connect to the server with the session ID of the remote client to which it needs to connect to. The server will check its data base and will establish data path between the remote and controller client, if valid session ID is provided by the controller client. Server uses certificate for SSL connections.

# Technical Support and Troubleshooting:
Scenario: A technical support team needs to provide assistance to customers who are experiencing issues with their software or systems.
Use Case: Customers install the remote client on their systems and connect to the server in cloud. The support team uses the controller client to connect to the same server and diagnose and troubleshoot issues by remotely accessing the customers' systems and executing commands.

# Remote Software Deployment:
Scenario: A software development team needs to deploy updates or patches to a distributed network of devices or servers.
Use Case: The development team uses the controller client to connect to the server in cloud and remotely execute deployment scripts or commands on the remote clients. This allows for efficient and coordinated software deployment across multiple devices or servers.
Session Identification: Both the remote client and the controller client provide identifiers when connecting to the server. The server matches the IDs and connects the controller client to corresponding remote client.
Multi-client Support: The server supports multiple simultaneous client connections, securely over SSL. 
Simultaneous Connections: Handles multiple connections and disconnections of clients with server without having to restart the server. The maximum number of remote clients at a time can be varied if needed.
Asynchronous I/O: The system utilizes asynchronous I/O operations to efficiently handle communication between multiple clients and the server without utilizing large OS resources.
SSL/TLS Encryption: The system utilizes the OpenSSL library to implement SSL/TLS encryption for secure communication between clients and the server. This ensures that data transmitted over the internet is encrypted.
Error Handling: The system incorporates error handling mechanisms to deal with various error scenarios, such as connection failures, invalid input, and SSL handshake failures. This enhances the reliability and robustness of the system.

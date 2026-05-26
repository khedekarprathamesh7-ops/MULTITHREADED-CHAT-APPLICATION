# MULTITHREADED-CHAT-APPLICATION

COMPANY : CODTECH IT SOLUTIONS

NAME : PRATHAMESH  SUNIL KHEDEKAR

INTERN ID : CTIS9258

DOMAIN  : JAVA 

DURATIONS : 4 WEEKS

MENTOR : NEELA SANTOSH

This project is a multithreaded chat application developed using Java Sockets and multithreading concepts. The main purpose of the application is to enable multiple users to communicate with each other in real time through a client-server architecture. The system consists of one server and multiple clients. The server acts as the central communication point, while clients connect to it and exchange messages. To support multiple users simultaneously, the application uses threads, ensuring that communication remains smooth and responsive without one user blocking another.

The project contains three major Java files: Server.java, ClientHandler.java, and Client.java. Each file has a specific responsibility in the operation of the chat system. The Server.java file is responsible for creating and managing the server. It initializes a ServerSocket on a specified port number, such as port 5000, and continuously waits for client connection requests. Once a client requests a connection, the server accepts it and creates a new ClientHandler object to manage that particular client.

The ClientHandler.java file is one of the most important components of the application. It implements the Runnable interface, allowing it to execute within a separate thread. Every time a new user connects to the server, a dedicated thread is created for that user. This design allows multiple clients to communicate at the same time. Without multithreading, the server would process clients one by one, causing delays and limiting the application to a single user interaction at a time.

The server maintains a collection of connected clients using a synchronized set. This collection stores references to all active client handlers. Synchronization ensures thread safety because multiple threads may attempt to access or modify the client list simultaneously. Whenever a client sends a message, the server uses a broadcast mechanism to distribute that message to all other connected clients. The broadcast method loops through the client collection and forwards the message to each active user except the sender. This allows all users in the chat application to receive updates instantly.

The Client.java file acts as the client-side application. It establishes a connection with the server using a socket and enables users to participate in the chat session. The client handles two tasks simultaneously: sending messages and receiving messages. To accomplish this, a separate thread is used to continuously listen for incoming messages from the server while the main thread accepts user input from the keyboard. This ensures that users can send and receive messages in real time without interruption.

Sockets are a key part of this project because they provide communication channels between the server and clients. A ServerSocket listens for incoming connections, while a Socket object creates communication between individual clients and the server. Input and output streams such as BufferedReader and PrintWriter are used to read and send messages efficiently.

Overall, this project successfully demonstrates the implementation of networking and multithreading concepts in Java. It provides real-time communication among multiple users, uses concurrent programming for better performance, and illustrates practical use of sockets in client-server application development. The application fulfills the objective of creating a functional multi-user chat system.

OUTPUT : <img width="1017" height="343" alt="Image" src="https://github.com/user-attachments/assets/abf17cc7-6629-41e3-9f43-c09ae163bd15" />
<img width="1020" height="347" alt="Image" src="https://github.com/user-attachments/assets/dc4f26b5-cc9e-4658-a7d2-2e1f27ea4346" />
<img width="1016" height="344" alt="Image" src="https://github.com/user-attachments/assets/9373925e-9c16-4573-b98d-5d8ef8488c16" />

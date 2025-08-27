# Chat Application (Java Sockets)

Author: Kathiravan S P
Tech Stack: Java, Socket Programming, OOP

# About

A real-time chat application built using Java sockets that allows multiple users to communicate with each other through a client-server model. This project demonstrates networking in Java, object-oriented principles, and modular code design.

# Who It’s For

Students learning Java Networking

Beginners exploring client-server architecture

Developers who want to understand multithreading in Java

Anyone looking for a simple messaging app in Java

# How It Works

Server – Listens for incoming client connections and manages broadcasting messages.

Client – Connects to the server and enables users to send/receive messages.

Multi-threading – Each client runs in a separate thread, ensuring real-time communication.

OOP Concepts – Uses Encapsulation, Inheritance, and Polymorphism to design the system.

# Features

Real-time text messaging

Supports multiple clients simultaneously

Handles clean client disconnections

## UML Diagram

```mermaid
classDiagram
    class Server {
      +startServer()
      +broadcast()
      -clientList[]
    }

    class Client {
      +connectServer()
      +sendMessage()
      +receiveMessage()
    }

    class ClientThread {
      +run()
      -socket
      -inputStream
      -outputStream
    }

    Server "1" o-- "*" Client
    Server "1" --> "*" ClientThread


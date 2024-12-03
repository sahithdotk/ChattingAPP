# ChattingAPP
This is a project that uses Java as the core language to develop the frontend for a Chatting application for universities and Organizations.

## Features

1. **Real-Time Messaging**:
   - Users can send and receive messages instantly.
   - Messages are broadcasted to all connected clients in a group chat setup.

2. **End-to-end encryption**:
   - The messages will be encrypted in the sender's side to be decrypted after recieving.

3. **User-Friendly GUI**:
   - Built using Java Swing, the application offers an easy-to-navigate interface for users.

4. **Extensibility**:
   - The modular design allows developers to easily add features like private messaging, message encryption, or multimedia support.

---

## Getting Started

### Prerequisites

- **Java Development Kit (JDK)** version 11 or above
- An IDE such as Visual Studio Code, IntelliJ IDEA, Eclipse, or NetBeans (optional)
- **PostgreSQL** database installed on your system

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sahithdotk/ChattingAPP
   ```

2. Navigate to the project directory:
   ```bash
   cd Chatting_Application
   ```

3. Compile the source code:
   ```bash
   javac Chatting_Application/src/*.java
   ```

4. Set up the PostgreSQL database:
   - Install PostgreSQL if not already installed:
     ```bash
     sudo apt update
     sudo apt install postgresql postgresql-contrib
     ```
   - Start the PostgreSQL service:
     ```bash
     sudo service postgresql start
     ```
   - Log in to the PostgreSQL shell:
     ```bash
     sudo -u postgres psql
     ```
   - Create a new database and table:
     ```sql
     CREATE DATABASE chatapp;
     \c chatapp
     CREATE TABLE chat_logs (
         id SERIAL PRIMARY KEY,
         sender VARCHAR(50),
         content TEXT,
         timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```

5. Run the server:
   ```bash
   java src/chatting/application/UserA.java
   ```

6. Run the client:
   ```bash
   java src/chatting/application/UserB.java
   ```
7. To display the logged chats in pgAdmin's Query tool:
   ```sql
   SELECt * FROM chat_Logs;
   ```

---

## Contributions

Contributions are welcome! If you'd like to add features, improve the code, or fix bugs, feel free to fork the repository and submit a pull request.

---

## License

This project is licensed under the [MIT License](LICENSE).

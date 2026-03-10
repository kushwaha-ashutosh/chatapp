# 💬 Real-Time Chat Rooms

A real-time chat application built with **Java Spring Boot** and **WebSockets**, enabling users to communicate instantly across multiple chat rooms.

---

## ✨ Features

- ⚡ **Real-time messaging** — instant message delivery with zero polling
- 🏠 **Multiple chat rooms** — join and switch between rooms seamlessly
- 👤 **User session management** — persistent user identity throughout the session
- 📡 **Instant message broadcasting** — messages delivered to all room participants simultaneously
- 🏗️ **Scalable backend architecture** — designed to handle concurrent connections efficiently

---

## 🏗️ System Architecture

```
Client (Browser)
       │
       │  WebSocket Connection
       ▼
  Chat Server (Spring Boot)
       │
       │  Message Processing
       ▼
  WebSocket Handler / STOMP Broker
       │
       │  Broadcast
       ▼
  Connected Clients (Chat Room)
```

---

## ⚙️ Tech Stack

| Layer              | Technology           |
|--------------------|----------------------|
| Backend            | Java / Spring Boot   |
| Real-time Comms    | WebSockets (STOMP)   |
| Database           | MySQL *(optional)*   |
| Build Tool         | Maven                |
| Frontend           | HTML / JS *(client)* |

---

## 📦 Getting Started

### Prerequisites

- Java 11+
- Maven 3.6+
- MySQL *(optional, for message persistence)*

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/kushwaha-ashutosh/chatapp.git
   ```

2. **Navigate to the project directory**
   ```bash
   cd chatapp
   ```

3. **Build the project**
   ```bash
   mvn clean install
   ```

4. **Run the application**
   ```bash
   mvn spring-boot:run
   ```

5. **Open your browser** and navigate to:
   ```
   http://localhost:8080
   ```

---

## 💡 Key Concepts Demonstrated

- **Real-time messaging systems** — event-driven architecture for instant communication
- **WebSocket communication** — full-duplex communication over a single TCP connection
- **Backend API design** — RESTful endpoints alongside WebSocket handlers
- **Scalable chat architecture** — room-based message routing and session tracking

---

## 📁 Project Structure

```
chatapp/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/chatapp/
│   │   │       ├── config/          # WebSocket configuration
│   │   │       ├── controller/      # Message & room controllers
│   │   │       ├── model/           # Message, User, Room models
│   │   │       └── service/         # Business logic
│   │   └── resources/
│   │       ├── static/              # Frontend assets
│   │       └── application.properties
│   └── test/
├── pom.xml
└── README.md
```

---

## 📈 Roadmap

- [ ] Private messaging between users
- [ ] User authentication & authorization (JWT)
- [ ] Message persistence with MySQL
- [ ] Push notifications
- [ ] Media & file sharing
- [ ] Read receipts
- [ ] Online/offline user indicators

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please open an issue first to discuss any major changes.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/kushwaha-ashutosh">Ashutosh Kushwaha</a>
</p>

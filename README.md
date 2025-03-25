# VoxaChat

A real-time chat application built with Java, Spring Boot, and Swing GUI, featuring WebSocket communication for instant messaging capabilities.

![Login Screen](screenshots/login-screen.png)

## Features

- Real-time messaging using WebSocket
- Modern Swing-based GUI with a clean interface
- User presence tracking (shows connected users)
- Responsive design that adapts to window resizing
- Secure message handling
- Cross-platform compatibility

## Screenshots

### Login Screen

![Login Screen](screenshots/login-screen.png)

### Chat Interface

![Chat Interface](screenshots/chat-interface.png)

## Tech Stack

- **Backend:**

  - Java 22
  - Spring Boot 3.3.2
  - Spring WebSocket
  - Maven

- **Frontend:**
  - Java Swing
  - Custom GUI components
  - WebSocket client implementation

## Project Structure

```
src/main/java/com/example/websocket_demo/
├── client/                     # Client-side code
│   ├── App.java                # Client application entry point
│   ├── ClientGUI.java          # Main Swing GUI implementation
│   ├── MessageListener.java    # Interface for message events
│   ├── MyStompClient.java      # WebSocket client implementation
│   ├── MyStompSessionHandler.java # WebSocket session handler
│   └── Utilities.java          # GUI utilities
├── Message.java                # Message data model
├── WebsocketConfig.java        # WebSocket configuration
├── WebsocketController.java    # WebSocket endpoint controller
├── WebsocketDemoApplication.java # Main Spring Boot application
└── WebSocketSessionManager.java # Session management
```

## Prerequisites

- Java 22 or later
- Maven 3.6 or later
- Internet connection for WebSocket communication

## Installation

1. Clone the repository:

```bash
git clone https://github.com/apexryan/VoxaChat.git
```

2. Navigate to the project directory:

```bash
cd VoxaChat
```

3. Build the project using Maven:

```bash
mvn clean install
```

4. Run the application:

```bash
mvn spring-boot:run
```

## Usage

1. Launch the application
2. Enter your username when prompted (maximum 16 characters)
3. Start chatting with other connected users
4. Messages are sent by pressing Enter or clicking the Send button
5. The connected users panel on the left shows all active participants
6. To exit, close the window and confirm when prompted

## Architecture

VoxaChat follows a client-server architecture:

- **Server**: Spring Boot application handling WebSocket connections, message routing, and user session management
- **Client**: Java Swing desktop application that connects to the server via WebSocket
- **Communication**: STOMP protocol over WebSocket for real-time messaging
- **Data Flow**: Messages sent from clients are processed by the server and broadcasted to all connected clients

## Deployment

The backend is deployed on Render.com. To deploy your own instance:

1. Create a Render.com account
2. Create a new Web Service
3. Connect your GitHub repository
4. Configure the following:
   - Build Command: `mvn clean install`
   - Start Command: `mvn spring-boot:run`
   - Environment Variables: Configure as needed

## Building Executable

To create an executable JAR file:

```bash
mvn clean package
```

The executable will be generated in the `target` directory.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Spring Boot team for the excellent framework
- All contributors and users of the application

## Contact

Ryan - [itsryan.kr@gmail.com](mailto:itsryan.kr@gmail.com)

Project Link: [https://github.com/apexryan/VoxaChat](https://github.com/apexryan/VoxaChat)

# Voxa

A real-time chat application built with Java, Spring Boot, and Swing GUI, featuring WebSocket communication for instant messaging capabilities.

## Features

- Real-time messaging using WebSocket
- Modern Swing-based GUI with a clean interface
- User presence tracking (shows connected users)
- Responsive design that adapts to window resizing
- Secure message handling
- Cross-platform compatibility

## Screenshots

### Login Screen

![Screenshot 2025-03-25 114447](https://github.com/user-attachments/assets/94af8cb0-0799-4b00-a4fe-7633580cc7f6)

### Chat Interface

![Screenshot 2025-03-25 114504](https://github.com/user-attachments/assets/351d768e-0766-4786-9de8-5f2a38b97cee)


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
Run app.java 
```

## Usage

1. Launch the application
2. Enter your username when prompted (maximum 16 characters)
3. Start chatting with other connected users
4. Messages are sent by pressing Enter or clicking the Send button
5. The connected users panel on the left shows all active participants
6. To exit, close the window and confirm when prompted

## Architecture

Voxa follows a client-server architecture:

- **Server**: Spring Boot application handling WebSocket connections, message routing, and user session management
- **Client**: Java Swing desktop application that connects to the server via WebSocket
- **Communication**: STOMP protocol over WebSocket for real-time messaging
- **Data Flow**: Messages sent from clients are processed by the server and broadcasted to all connected clients

## Deployment

The backend is deployed on Render.com. To deploy your own instance:

1. Create a Render.com account
2. Create a new Web Service
3. Connect your GitHub repository
4. Select the repo, dockerfile will handle the rest
5. Deploy Web Service

## Building Executable

To create an executable JAR file:

```bash
Open IntelliJ IDEA

Navigate to:
File → Project Structure → Artifacts → + → JAR → Jar from module with dependencies

Select the Main Class containing public static void main(String[] args)

Set the output directory for the JAR file

Click Apply → OK

Build the artifact:
Build → Build Artifacts → Build
```

The executable will be generated in the `target` directory.

## Contributing

Contributions are not accepted at this time.

## License

This project is licensed under the All Rights Reserved. - see the LICENSE file for details.

## Acknowledgments

- Spring Boot team for the excellent framework
- All contributors and users of the application

## Contact

Rupayan - [itsryan.kr@gmail.com](mailto:itsryan.kr@gmail.com)

Project Link: [https://github.com/apexryan/VoxaChat](https://github.com/apexryan/VoxaChat)

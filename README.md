Chat Application
================

Overview
--------

This is a simple real-time chat application built using the **Travel Reverb**, **Vue.js**, **SQLite**, and **Laravel**. The application allows users to send and receive messages in real time. It is a web-based chat system that leverages Laravel for the backend, Vue.js for the frontend, and SQLite as the database engine.

Features
--------

-   **User Authentication**: Users can sign up and log in to the chat system.
-   **Real-Time Messaging**: Instant communication using Travel Reverb for real-time broadcasting.
-   **Responsive Design**: Works on both desktop and mobile devices.
-   **SQLite Integration**: Lightweight database used for storing user and message data.
-   **Message History**: Users can view previous messages from the chat history.
-   **Real-Time Notifications**: Receives notifications when new messages arrive.

Technology Stack
----------------

-   **Laravel**: Backend framework to handle API requests, routing, authentication, and database management.
-   **Vue.js**: Frontend JavaScript framework used for building the user interface.
-   **Travel Reverb**: Laravel package used for broadcasting events and enabling real-time communication.
-   **SQLite**: Lightweight, file-based database for storing user and message data.

Core Components
---------------

1.  **Backend** (Laravel)

    -   RESTful API for managing user authentication and message retrieval.
    -   WebSocket broadcasting with Travel Reverb for real-time communication.
    -   SQLite database for storing messages, user data, and chat sessions.
2.  **Frontend** (Vue.js)

    -   **Chat Component**: Handles real-time message display and user interaction.
    -   **Message Input**: Allows users to type and send messages to the chat.
    -   **Authentication Views**: Login and registration forms for user access control.
3.  **Database** (SQLite)

    -   Stores user information, including credentials and chat messages.

Key Files & Folders
-------------------

-   **Laravel Backend**:

    -   `routes/web.php`: Defines routes for the application.
    -   `app/Http/Controllers/ChatController.php`: Handles the chat functionality.
    -   `app/Models/Message.php`: Model to manage message data.
    -   `database/migrations/`: Contains the migration files for the database schema.
    -   `config/broadcasting.php`: Configures the Travel Reverb settings.
-   **Vue.js Frontend**:

    -   `resources/js/components/ChatComponent.vue`: Core Vue component for the chat interface.
    -   `resources/js/app.js`: Initializes Vue and connects to Laravel Echo for WebSocket handling.
-   **SQLite Database**:

    -   `database/database.sqlite`: SQLite database storing user data and chat history.

API Endpoints
-------------

-   `POST /login`: Authenticate user and return token.
-   `POST /register`: Register a new user.
-   `GET /messages`: Retrieve the chat history.
-   `POST /messages`: Send a new message.

How It Works
------------

1.  **User Registration and Authentication**:

    -   Users sign up and log in using Laravel's authentication system. Once logged in, they can start chatting.
2.  **Real-Time Messaging**:

    -   When a user sends a message, the message is stored in the SQLite database.
    -   Travel Reverb broadcasts the message to all connected clients in real time, enabling live chat updates.
3.  **Chat Interface**:

    -   The chat interface is built using Vue.js. When new messages are received via Travel Reverb, they are dynamically added to the message feed.

Future Improvements
-------------------

-   Add support for private messaging between users.
-   Implement file sharing (images, documents) in chat.
-   Add typing indicators and read receipts.
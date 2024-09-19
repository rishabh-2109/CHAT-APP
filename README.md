# chat-app
A real-time chat application developed using the MERN stack (MongoDB, Express.js, React, and Node.js), integrated with Socket.IO for live communication.

NAME-RISHABH SHARMA       
COLLEGE-IIT JAMMU

                                        System Design Document for Messaging Service Prototype
  1. Overview
This system is a real-time chat application built using the MERN stack (MongoDB, Express.js, React, and Node.js) with Socket.IO to enable real-time communication. It allows users to sign up, log in, and chat with other users in real-time. The system employs secure authentication mechanisms using JSON Web Tokens (JWT) and provides a responsive user interface for a seamless experience across devices.

2. Architecture Overview
Frontend: React.js is used for the client-side of the application, providing a responsive UI and handling user interactions. Socket.IO is integrated to establish real-time communication with the server.

Backend: Node.js and Express.js manage the server-side operations, including handling API requests, managing user authentication (with JWT), and facilitating WebSocket connections via Socket.IO.

Database: MongoDB is used for storing user data, including credentials, and chat messages. MongoDB’s flexible schema allows efficient storage and retrieval of data related to real-time chats.

Real-time Communication: Socket.IO is utilized for bi-directional communication between the client and server, enabling the real-time exchange of messages.

3. Features
User Sign-up: Users can create an account by providing a unique username and password. This information is stored securely in the MongoDB database.

User Sign-in: Registered users can log in using their credentials, which are authenticated using JWT for secure access.

Real-time Chat: Once authenticated, users can engage in real-time chat conversations with other users. Messages are instantly transmitted and displayed without refreshing the page.

JWT-Based Authentication: JWT tokens are used for secure authentication. When a user logs in, a JWT is generated, which is used to authorize subsequent API requests.

Responsive UI: The UI is designed using React and CSS frameworks, ensuring it adapts to different screen sizes, providing a consistent experience across devices   .

4. System Workflow
User Authentication:
The user signs up and provides a username and password.
Password is hashed and stored in MongoDB.
On login, a JWT is issued if the credentials are valid.

Establishing Socket.IO Connection:
Upon successful authentication, the client connects to the WebSocket server.
The user joins a room, enabling real-time communication with others in that room.

Real-time Messaging:
Messages are sent via Socket.IO.
The server receives the message and broadcasts it to other connected clients.
Messages are stored in MongoDB for future retrieval.

5. Dependencies and Libraries
React.js: Chosen for building the frontend as it provides a fast, efficient, and component-based approach for building user interfaces.

Node.js and Express.js: Node.js is used for its non-blocking, event-driven architecture, which is suitable for real-time applications. Express.js is a minimalist web framework that simplifies server-side routing.

MongoDB: A NoSQL database that provides flexibility in storing user credentials and chat messages. Its document-based model is ideal for real-time applications.

Socket.IO: Enables real-time, bi-directional communication between the client and server, making it suitable for chat applications.

JWT (jsonwebtoken package): JWT is used to ensure secure user authentication and authorization.

Bcrypt: Used to hash passwords securely before storing them in MongoDB.

                                                           Setup Documentation
Prerequisites:
Node.js and npm should be installed on your machine.
MongoDB: A MongoDB server should be running locally or via a cloud service (e.g., MongoDB Atlas).

Steps to Set Up the Project:
1. Clone the repository:
git clone <repository-url>
cd chat-app
2. Install Backend Dependencies:
cd server
npm install
3. Install Frontend Dependencies:
cd ../client
npm install
4. Configure Environment Variables:
MONGO_URI=mongodb://localhost:27017/chat-app
JWT_SECRET=<your-jwt-secret>
5. Run the Backend Server:
 cd server
 npm start
6. Run the Frontend Server:
cd client
npm run dev





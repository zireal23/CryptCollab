## End-to-End Encrypted Collaboration System
![System Image](cryptCollab.png)
Welcome to the README file for the end-to-end encrypted collaboration system! This system is designed to provide a secure environment for collaborative document editing, similar to Google Docs, while leveraging the security of WhatsApp. Below you will find important information about the system, its architecture, and the key technologies used in its development.

### Overview

The end-to-end encrypted collaboration system follows a server-client model, where the backend is built in Node.js with an Express server. The backend provides registration and authentication capabilities using JSON Web Tokens (JWT). Additionally, a WebSocket server, built with Socket.IO, is employed to create collaborative rooms for sessions.

The user data is stored in a Redis database, ensuring efficient data retrieval and management. To enhance system reliability and scalability, multiple instances of the server are deployed, and Redis Emitter is utilized as a communication channel between the instances to facilitate data synchronization.

On the frontend, the system is built with React and Redux, leveraging the Context API for state management. The client-side cryptography plays a pivotal role in ensuring the security of the system. A custom library called x3dh is developed to handle the Diffie-Hellman key exchange process securely. The generated keys are then stored in an encrypted form using the Secure Web Store, which utilizes IndexedDB as the storage mechanism.

### Key Technologies Used

1. **Backend**:

   - Node.js: A JavaScript runtime environment for building the server-side logic.
   - Express: A web application framework for Node.js, providing routing and middleware capabilities.
   - JWT (JSON Web Tokens): Used for secure user authentication and authorization.
   - Socket.IO: Enables real-time, bidirectional communication between the server and clients using WebSockets.

2. **Database**:

   - Redis: A fast and efficient in-memory data structure store used for storing user data, ensuring quick access and data persistence.

3. **Communication and Synchronization**:

   - Redis Emitter: Provides a communication channel between multiple server instances to synchronize data and maintain system integrity.

4. **Frontend**:

   - React: A popular JavaScript library for building user interfaces, enabling efficient and modular UI components.
   - Redux: A predictable state container for JavaScript apps, facilitating state management and data flow.
   - Context API: A built-in React feature for managing global state and sharing data between components.

5. **Cryptography**:
   - x3dh: A custom library developed for the Diffie-Hellman key exchange, ensuring secure key generation and exchange between clients.
   - Secure Web Store: A client-side storage solution that encrypts and securely stores the generated cryptographic keys in IndexedDB.

### Installation and Setup

To set up the end-to-end encrypted collaboration system, follow the steps below:

1. Clone the repository: `git clone https://github.com/zireal23/CryptCollab.git`
2. Install backend dependencies: `npm install`
3. Install frontend dependencies: `cd frontend && npm install`
4. Configure the backend:
   - Set up the Redis database connection details.
   - Configure JWT settings for authentication.
   - Configure server instances and communication channels.
5. Configure the frontend:
   - Set up the WebSocket server URL.
   - Configure API endpoints for backend communication.
6. Build the frontend: `npm run build` (generates the production-ready frontend code)
7. Start the server: `npm start`
8. Access the system through the provided URL.

### Contributing

Contributions to the end-to-end encrypted collaboration system are welcome! If you have any ideas, suggestions, or bug fixes, please submit them as issues or create a pull request with the proposed changes. Remember to adhere to the project's code style guidelines and include appropriate tests for your contributions.

### License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code for personal or commercial purposes.

### Contact

If you have any questions or need further assistance, please feel free to contact the project maintainers at [skasif232000@gmail.com](mailto:skasif232000@gmail.com).

Thank you for using the end-to-end encrypted collaboration system! We hope you find it useful and secure for your collaborative document editing needs.

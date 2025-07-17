# QuickChat - Real-time Messaging Application

QuickChat is a modern, full-stack chat application designed for seamless real-time communication. It allows users to sign up, log in, manage their profiles, and engage in instant messaging with other users, including sending text messages and images. The application is built with a focus on a responsive user interface and efficient backend services.

## ✨ Features

### User Management
* **User Authentication**: Secure signup and login functionalities.
* **Profile Management**: Users can update their full name, bio, and profile picture.
* **Logout Functionality**: Securely log out from the application.

### Real-time Chat
* **Instant Messaging**: Send and receive text messages in real time.
* **Image Sharing**: Users can send images in their chats.
* **Online Status**: View the online/offline status of other users.
* **Unseen Message Count**: Displays the number of unread messages for each chat.
* **Message Seen Status**: Messages are marked as seen when viewed by the recipient.
* **Search Users**: Easily search for other users to start a chat.
* **Media Gallery**: View all images shared within a chat in a dedicated media section.

### Technical Highlights
* **Token-based Authentication**: Utilizes JWT (JSON Web Tokens) for secure authentication and authorization.
* **Cloudinary Integration**: Seamlessly handles image uploads and storage.
* **Socket.io**: Powers real-time, bidirectional communication between the client and server.
* **Environment Variables**: Securely manages sensitive configuration data using `.env` files.

## 💻 Technologies Used

**Client-Side:**
* **React v19.1.0**: A JavaScript library for building user interfaces.
* **Vite v7.0.1**: A fast build tool for modern web projects.
* **Tailwind CSS v4.1.11**: A utility-first CSS framework for rapid UI development.
* **React Router DOM v7.6.3**: Declarative routing for React applications.
* **Axios v1.10.0**: Promise-based HTTP client for the browser and Node.js.
* **React Hot Toast v2.5.2**: Lightweight and customizable toast notifications.
* **Socket.io Client v4.8.1**: Client-side library for Socket.io.

**Server-Side:**
* **Node.js**: JavaScript runtime environment.
* **Express v5.1.0**: Fast, unopinionated, minimalist web framework.
* **MongoDB**: NoSQL database for storing application data.
* **Mongoose v8.16.3**: MongoDB object modeling for Node.js.
* **Socket.io v4.8.1**: Server-side library for real-time communication.
* **bcryptjs v3.0.2**: Library for hashing passwords.
* **jsonwebtoken v9.0.2**: JSON Web Token implementation.
* **Cloudinary v2.7.0**: Cloud-based image and video management.
* **CORS v2.8.5**: Middleware for enabling Cross-Origin Resource Sharing.
* **dotenv v17.2.0**: Loads environment variables from a `.env` file.
* **Nodemon v3.1.10**: Utility that monitors for changes in your Node.js application and automatically restarts the server.

## 🚀 Installation and Setup

### Prerequisites
* Node.js (LTS version recommended)
* MongoDB installed locally or a cloud-based MongoDB Atlas account.

### Steps

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd wannaseemefall/chat-app/chat-app-f6552d5119d34dced10a5f878d90c52b79940fa0
    ```

2.  **Server Setup:**
    * Navigate to the `server` directory:
        ```bash
        cd server
        ```
    * Install dependencies:
        ```bash
        npm install
        ```
    * Create a `.env` file in the `server` directory with the following content:
        ```
        MONGODB_URI="your_mongodb_connection_string"
        JWT_SECRET="your_jwt_secret_key"
        CLOUDINARY_CLOUD_NAME="your_cloudinary_cloud_name"
        CLOUDINARY_API_KEY="your_cloudinary_api_key"
        CLOUDINARY_API_SECRET="your_cloudinary_api_secret"
        PORT=5001 # Optional, default is 5001
        ```
        * Replace placeholders with your actual MongoDB connection string, a strong JWT secret, and Cloudinary API credentials.
    * Start the server:
        ```bash
        npm run server
        # Or for production: npm start
        ```
        The server will run on `http://localhost:5001` (or your specified PORT).

3.  **Client Setup:**
    * Navigate to the `client` directory:
        ```bash
        cd ../client
        ```
    * Install dependencies:
        ```bash
        npm install
        ```
    * Create a `.env` file in the `client` directory with the following content:
        ```
        VITE_BACKEND_URL="http://localhost:5001" # Or your deployed backend URL
        ```
    * Start the development server:
        ```bash
        npm run dev
        ```
        The client application will typically open in your browser at `http://localhost:5173` (or another available port).

## 🚀 Usage

Once the client and server are running:
1.  **Sign Up**: Create a new account on the login page by providing your full name, email, password, and a short bio.
2.  **Login**: Use your registered credentials to log in.
3.  **Chat**: On the home page, you will see a list of available users. Click on a user to start a conversation.
4.  **Send Messages**: Type your message in the input field and press Enter or click the send button.
5.  **Send Images**: Click the gallery icon in the chat input to upload and send images.
6.  **Edit Profile**: Access the "Edit Profile" option from the sidebar menu to update your profile details and profile picture.

## ⚙️ Deployment

This project is designed for easy deployment.
* The **server-side** is configured for deployment on Vercel.
* The **client-side** (React application) can also be deployed on Vercel or any static hosting service.

## 🤝 Contributing

Contributions are welcome! Please feel free to fork the repository, make your changes, and submit a pull request.

## 📄 License

This project is licensed under the MIT License - see the `package.json` files in both `client` and `server` directories for details.

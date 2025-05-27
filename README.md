# News Media Platform

A full-stack MERN application for a news media platform with features like user authentication, article publishing, commenting, and more.

## Features

- User authentication (register, login, JWT)
- User roles (reader, author, admin)
- Article management (create, read, update, delete)
- Categories for articles
- Comments on articles
- Search and filter functionality
- Responsive design

## Tech Stack

- MongoDB: Database
- Express.js: Backend API
- React.js: Frontend UI
- Node.js: Server environment
- Bootstrap: Styling
- Axios: HTTP requests
- JWT: Authentication

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)

### Installation

1. Clone the repository
   ```
   git clone <repository-url>
   cd news-media-platform
   ```

2. Install All Dependencies
   ```
   npm run install-all
   ```

3. Configure Environment Variables
   - Create a `.env` file in the server directory based on `.env.example`
   - Set up your MongoDB connection string and JWT secret

### Running the Application

To run both the client and server concurrently:
```
npm run dev
```

To run just the server:
```
npm run server
```

To run just the client:
```
npm run client
```

The server will run on http://localhost:5000 and the client on http://localhost:3000.

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login
- `GET /api/auth/me` - Get current user
- `GET /api/auth/logout` - Logout

### Articles
- `GET /api/articles` - Get all articles
- `GET /api/articles/:id` - Get a single article
- `POST /api/articles` - Create a new article (Author, Admin)
- `PUT /api/articles/:id` - Update an article (Author, Admin)
- `DELETE /api/articles/:id` - Delete an article (Author, Admin)

### Categories
- `GET /api/categories` - Get all categories
- `GET /api/categories/:id` - Get a single category
- `POST /api/categories` - Create a new category (Admin)
- `PUT /api/categories/:id` - Update a category (Admin)
- `DELETE /api/categories/:id` - Delete a category (Admin)

### Comments
- `GET /api/articles/:articleId/comments` - Get all comments for an article
- `POST /api/articles/:articleId/comments` - Add a comment to an article
- `PUT /api/comments/:id` - Update a comment
- `DELETE /api/comments/:id` - Delete a comment

### Users (Admin only)
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get a single user
- `POST /api/users` - Create a new user
- `PUT /api/users/:id` - Update a user
- `DELETE /api/users/:id` - Delete a user 
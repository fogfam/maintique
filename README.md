# Maintique

A platform for antique maintenance and collection.

## Setup

1. Clone the repository
2. Install dependencies with `npm install`
3. Create a `.env` file based on `.env.example` with your MongoDB connection string and JWT secret
4. Run the development server with `npm run dev`

## API Endpoints

### Authentication

- `POST /api/users` - Register a new user
  - Body: `{ name, email, password }`
  - Returns: JWT token

- `POST /api/auth` - Login a user
  - Body: `{ email, password }`
  - Returns: JWT token

- `GET /api/auth` - Get logged in user info
  - Headers: `x-auth-token: YOUR_JWT_TOKEN`
  - Returns: User object (without password)

## Database

The application uses MongoDB. Make sure to set up your database connection string in the `.env` file.
# Ananda Beauty Parlour Booking System

A comprehensive MERN stack application for managing beauty parlour bookings. This application allows users to book beauty services, and enables administrators to manage services, stylists, and bookings.

## Features

### User Features
- User registration and login
- Browse services and stylists
- Book appointments by selecting service, date, and time
- View and manage personal bookings
- Cancel bookings

### Admin Features
- Comprehensive dashboard with revenue analytics
- Manage bookings (confirm, cancel, mark as completed)
- Add and manage services
- Add and manage stylists
- View booking statistics

## Technology Stack

### Frontend
- React.js with TypeScript
- TailwindCSS for styling
- React Router for navigation
- SweetAlert2 for notifications
- Axios for API requests
- JWT for authentication

### Backend
- Node.js with Express
- MongoDB with Mongoose
- JWT for authentication
- bcrypt for password hashing
- Express-validator for request validation

## Setup Instructions

### Prerequisites
- Node.js (v14+)
- MongoDB (local or Atlas)

### Backend Setup
1. Navigate to the backend directory:
   ```
   cd backend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a .env file based on .env.example:
   ```
   cp .env.example .env
   ```

4. Update the .env file with your MongoDB URI and JWT secret

5. Start the backend server:
   ```
   npm run dev
   ```

### Frontend Setup
1. Navigate to the project root directory

2. Install dependencies:
   ```
   npm install
   ```

3. Start the frontend development server:
   ```
   npm run dev
   ```

## API Endpoints

### Authentication
- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login user

### Users
- GET /api/users/profile - Get current user profile
- PUT /api/users/profile - Update user profile

### Bookings
- GET /api/bookings - Get all bookings (admin only)
- GET /api/bookings/user - Get current user's bookings
- POST /api/bookings - Create a new booking
- GET /api/bookings/:id - Get booking by ID
- PATCH /api/bookings/:id/status - Update booking status (admin only)
- PATCH /api/bookings/:id/cancel - Cancel a booking
- DELETE /api/bookings/:id - Delete a booking (admin only)
- GET /api/bookings/available-slots - Get available time slots for a date

### Services
- GET /api/services - Get all services
- GET /api/services/:id - Get service by ID
- POST /api/services - Create a new service (admin only)
- PUT /api/services/:id - Update a service (admin only)
- DELETE /api/services/:id - Delete a service (admin only)
- GET /api/services/category/:category - Get services by category

### Stylists
- GET /api/stylists - Get all stylists
- GET /api/stylists/:id - Get stylist by ID
- POST /api/stylists - Create a new stylist (admin only)
- PUT /api/stylists/:id - Update a stylist (admin only)
- DELETE /api/stylists/:id - Delete a stylist (admin only)
- GET /api/stylists/specialization/:specialization - Get stylists by specialization

## Default Admin Account
To access admin features, you can create an admin account by using the registration endpoint and manually changing the role to 'admin' in the database, or create a seed script for initial data.

## License
This project is licensed under the MIT License.
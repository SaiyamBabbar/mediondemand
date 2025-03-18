# MediOnDemand - Installation Guide

This document provides detailed instructions for setting up the MediOnDemand application for development and production environments.

## Prerequisites

- Node.js (v18.0.0 or higher)
- MongoDB (v6.0 or higher)
- npm (v9.0.0 or higher) or yarn (v1.22.0 or higher)
- Git

## Development Setup

### Clone the Repository

```bash
git clone https://github.com/yourusername/MediOnDemand.git
cd MediOnDemand
```

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory and add the following environment variables:
   ```
   # Server Configuration
   PORT=5000
   NODE_ENV=development

   # MongoDB Configuration
   MONGO_URI=mongodb://localhost:27017/mediondemand

   # JWT Configuration
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRE=30d

   # Email Configuration
   EMAIL_SERVICE=gmail
   EMAIL_USERNAME=your_email@gmail.com
   EMAIL_PASSWORD=your_email_password
   EMAIL_FROM=noreply@mediondemand.com

   # AWS S3 Configuration
   AWS_ACCESS_KEY_ID=your_aws_access_key
   AWS_SECRET_ACCESS_KEY=your_aws_secret_key
   AWS_BUCKET_NAME=your_bucket_name
   AWS_REGION=your_aws_region

   # Stripe Configuration
   STRIPE_SECRET_KEY=your_stripe_secret_key
   STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret

   # Google Maps API
   GOOGLE_MAPS_API_KEY=your_google_maps_api_key
   ```

4. Start the backend server:
   ```bash
   # For development with nodemon
   npm run dev

   # For production
   npm start
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the frontend directory and add the following environment variables:
   ```
   REACT_APP_API_URL=http://localhost:5000/api
   REACT_APP_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
   REACT_APP_STRIPE_PUBLIC_KEY=your_stripe_public_key
   ```

4. Start the frontend development server:
   ```bash
   npm start
   ```

5. Open your browser and navigate to `http://localhost:3000` to view the application.

## Production Setup

### Backend Production Setup

1. Build the backend for production:
   ```bash
   cd backend
   npm run build
   ```

2. Start the production server:
   ```bash
   npm start
   ```

### Frontend Production Setup

1. Build the frontend for production:
   ```bash
   cd frontend
   npm run build
   ```

2. Serve the static files using a web server like Nginx or Apache.

## Docker Setup

### Prerequisites

- Docker (v20.10.0 or higher)
- Docker Compose (v2.0.0 or higher)

### Steps

1. Build and run the Docker containers:
   ```bash
   docker-compose up -d
   ```

2. Access the application at `http://localhost:3000`.

## Database Setup

### MongoDB Configuration

1. Create a MongoDB database named `mediondemand`.

2. The application will automatically create the required collections and indexes when it starts.

## Troubleshooting

### Common Issues

1. **Port already in use**: 
   - Change the port in the `.env` file and restart the server.

2. **MongoDB connection error**:
   - Ensure MongoDB is running.
   - Check the connection string in the `.env` file.

3. **JWT errors**:
   - Ensure the JWT secret is set correctly in the `.env` file.

4. **Email sending issues**:
   - Check the email configuration in the `.env` file.



Code Structure & Best Practices

Modular Architecture

Separation of concerns between frontend and backend
Component-based frontend structure
MVC pattern for backend organization


Clean Code Practices

Consistent naming conventions
Proper error handling
Comprehensive documentation
Security best practices


Version Control Best Practices

Meaningful commit messages
Feature branching workflow
Regular commits with clear purposes
   - If using Gmail, enable "Less secure app access" or use an app password.
   - Verify the AWS credentials and bucket name in the `.env` file.
   - Ensure the bucket has the appropriate permissions.

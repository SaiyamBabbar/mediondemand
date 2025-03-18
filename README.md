# MediOnDemand: On-Demand Nurses & Medical Equipment Rental

## Problem Statement

Healthcare facilities often face **staff shortages**, especially during peak times, emergencies, or night shifts. Patients recovering at home after surgery or elderly individuals also require **trained nurses and medical equipment** for proper care. Unfortunately, hiring professional caregivers on a **temporary basis** or renting **medical devices** is **challenging, expensive, and unorganized**.

Many hospitals struggle with **temporary staffing for nurses, ICU assistants, and OT technicians**, which affects patient care quality. Similarly, home patients **lack access to professional caregivers** and often **purchase costly medical equipment** when they only need it temporarily.

Our platform, **MediOnDemand**, aims to solve this problem by providing **on-demand nurses & medical equipment rental** for **hospitals, clinics, and home-based patients**, ensuring **affordable, reliable, and quick healthcare services.**

## Solution Overview

MediOnDemand is a comprehensive platform that connects healthcare facilities and patients with verified healthcare professionals and medical equipment providers. The platform serves as a marketplace where:

1. **Healthcare Professionals** (nurses, ICU assistants, OT technicians) can register, verify their credentials, set their availability, and offer their services.

2. **Medical Equipment Providers** can list their equipment for rent with detailed specifications, availability, and pricing.

3. **Healthcare Facilities & Patients** can search for healthcare professionals and equipment based on their requirements, location, and availability, and book them for specific time periods.

### Key Technologies Used

- **Frontend**: React.js, Redux, Material-UI
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Payment Integration**: Stripe
- **Geolocation**: Google Maps API
- **Notifications**: Socket.io, Nodemailer
- **File Storage**: AWS S3
- **Deployment**: Docker, AWS

## Setup & Installation

For detailed setup instructions, please refer to the [INSTALLATION.md](./INSTALLATION.md) file.

### Quick Start

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/MediOnDemand.git
   cd MediOnDemand
   ```

2. Install dependencies for both frontend and backend:
   ```
   # Install backend dependencies
   cd backend
   npm install

   # Install frontend dependencies
   cd ../frontend
   npm install
   ```

3. Set up environment variables:
   Copy the `.env.example` file to `.env` in both the frontend and backend directories and update the values accordingly.

4. Start the development servers:
   ```
   # Start backend server
   cd backend
   npm run dev

   # Start frontend server
   cd ../frontend
   npm start
   ```

5. Open your browser and navigate to `http://localhost:3000` to view the application.

## Usage Instructions

### For Healthcare Professionals

1. Register as a healthcare professional
2. Complete your profile with credentials, experience, and specializations
3. Set your availability and pricing
4. Accept booking requests from healthcare facilities and patients

### For Medical Equipment Providers

1. Register as a medical equipment provider
2. Add your equipment with details, images, and pricing
3. Manage inventory and availability
4. Process rental requests and handle returns

### For Healthcare Facilities & Patients

1. Register as a healthcare facility or patient
2. Search for healthcare professionals or medical equipment
3. Filter results based on location, availability, and requirements
4. Book professionals or equipment for specific time periods
5. Make payments and provide feedback

## API Documentation

### Authentication Endpoints

- **POST /api/auth/register**: Register a new user
- **POST /api/auth/login**: Log in an existing user
- **GET /api/auth/me**: Get current user information

### Nurse Endpoints

- **GET /api/nurses**: Get all nurses
- **GET /api/nurses/:id**: Get a specific nurse
- **POST /api/nurses**: Register as a nurse
- **PUT /api/nurses/:id**: Update nurse information
- **GET /api/nurses/available**: Get available nurses

### Equipment Endpoints

- **GET /api/equipment**: Get all equipment
- **GET /api/equipment/:id**: Get a specific equipment
- **POST /api/equipment**: Add new equipment
- **PUT /api/equipment/:id**: Update equipment information
- **GET /api/equipment/available**: Get available equipment

### Booking Endpoints

- **POST /api/bookings**: Create a new booking
- **GET /api/bookings**: Get all bookings
- **GET /api/bookings/:id**: Get a specific booking
- **PUT /api/bookings/:id**: Update booking status
- **GET /api/bookings/user**: Get bookings for current user

For detailed API documentation, refer to the [API Documentation](./api-docs.md) file.

## Demo Video


## Future Enhancements

1. Mobile applications for iOS and Android
2. Integration with health monitoring devices
3. Telemedicine consultations
4. Emergency response system
5. AI-powered recommendation system


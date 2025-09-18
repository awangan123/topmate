# **Topmate Backend - Express.js & MongoDB API**

## Description

**Topmate** is a backend application designed for a mentorship platform that connects users with mentors. The platform allows users to book services, browse available mentors, and manage their bookings. Built with **Express.js** and **MongoDB**, Topmate provides a robust and scalable API for both users and administrators to interact with the system in a seamless and efficient manner.

### Key Features

1. **User Authentication**: The backend API ensures secure login and registration through **JWT (JSON Web Tokens)**. Upon logging in, users receive a token that must be used to access restricted routes, ensuring that only authenticated users can book services and view their profiles.
   
2. **Mentor Management**: Mentors are a core part of this platform. Admin users have the ability to create, read, update, and delete mentor profiles. Mentors offer different services that users can browse through and book.
   
3. **Service Management**: Administrators can manage available services offered by mentors. Each service is associated with a mentor and can be booked by users.

4. **Booking System**: Users can book services offered by mentors. Once a service is booked, the user is provided with a booking confirmation, and the booking is stored in the database. The system allows users to view and update their bookings.

5. **Role-based Authorization**: The application differentiates between regular users and admins. Admins have higher privileges, such as the ability to add or remove mentors and services, while regular users can only interact with mentors and services (i.e., booking).

6. **Modular Code Structure**: The backend is built using a well-organized **Repository + Services + Routes + Controllers** architecture, which ensures maintainability and scalability. This architecture allows for easy modifications, clean separation of concerns, and easier unit testing of each part of the application.

7. **MongoDB Database**: MongoDB is used as the database for storing users, mentors, services, and bookings. It allows flexibility in storing different types of data and supports horizontal scaling for high-traffic applications.

8. **Error Handling**: The backend includes comprehensive error handling, with descriptive error messages to help users and developers quickly identify issues. Common errors such as invalid inputs, unauthorized access, or not found resources are handled gracefully with appropriate HTTP status codes.

9. **Security Features**: Passwords are hashed using **bcryptjs** before being stored in the database. This ensures that even in case of a data breach, user passwords are not exposed in plaintext. Additionally, **rate limiting** is applied to prevent abuse of the API.

### Goals and Use Case

The main goal of Topmate is to provide a scalable, secure, and efficient backend service for a mentorship platform. This service is ideal for anyone looking to build an online mentorship platform where mentors can offer personalized services to users. It allows admins to manage mentor profiles, services, and bookings while providing users with a simple and secure way to interact with the mentors and schedule sessions.

**Topmate Backend** can be extended and integrated with various frontend frameworks (e.g., React, Angular, Vue.js) to create a full-fledged web application. It's also highly customizable, so you can adapt the system to fit the specific needs of your mentorship platform.

## Tech Stack

- **Backend Framework**: [Express.js](https://expressjs.com/)
- **Database**: [MongoDB](https://www.mongodb.com/)
- **Object Data Mapper**: [Mongoose](https://mongoosejs.com/)
- **Authentication**: [JWT (JSON Web Tokens)](https://jwt.io/)
- **Password Hashing**: [bcryptjs](https://www.npmjs.com/package/bcryptjs)
- **Environment Variables**: [dotenv](https://www.npmjs.com/package/dotenv)
- **Validation**: [Joi](https://joi.dev/)

## Installation

### Prerequisites

Before starting, ensure you have the following software installed:

- **Node.js** (v14 or higher): [Install Node.js](https://nodejs.org/en/)
- **MongoDB** (local or using MongoDB Atlas): [Install MongoDB](https://www.mongodb.com/try/download/community)

### Clone the repository

Start by cloning the repository to your local machine:

```bash
git clone https://github.com/<your-username>/topmate-backend.git
cd topmate-backend

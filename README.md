# AirBnB Clone Project

## 🌟 Project Overview
This is a simplified clone of the popular Airbnb platform, created as part of the ALX Software Engineering Program. It replicates core functionalities such as listing properties, searching, and booking using a modular, scalable, and testable codebase.

## 🎯 Project Goals
- Understand the fundamentals of back-end web architecture.
- Build a dynamic web application using OOP in Python.
- Practice working with file storage, databases, and web frameworks.
- Learn to collaborate using Git, GitHub, and coding best practices.

## Technology Stack

The AirBnB Clone project uses the following technologies to build a robust and scalable web platform:

### 🐍 Python
Primary programming language used to develop backend logic and APIs.

### 🌐 Flask
A lightweight web framework for building RESTful APIs. Handles routing, request/response handling, and middleware integration.

### 🐬 MySQL
Relational database system used to store and manage structured data such as user accounts, property listings, bookings, etc.

### 🧪 Unittest
Python’s built-in testing framework used to write unit and integration tests to ensure code reliability and prevent regressions.

### 🔗 RESTful API
Architectural style used to design the backend API, enabling communication between the frontend (if applicable) and backend over HTTP.

### 🛠️ Git & GitHub
Version control system used for tracking changes and collaborating as a team. GitHub hosts the repository and allows for issue tracking and pull requests.

### ☁️ Linux/Ubuntu (CLI)
Used as the development environment, often with Bash commands and scripts to manage server configurations, run programs, and automate tasks.

### 🛡️ API Security
Best practices implemented to secure endpoints, authenticate users, and prevent vulnerabilities such as SQL injection and cross-site scripting (XSS).
## Database Design

The database design for the AirBnB Clone project includes several key entities that model the core features of the platform. Below is an overview of the primary entities, their important fields, and their relationships.

### 🧑 Users
- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `created_at`

**Relationship:** A user can own multiple properties and make multiple bookings. A user can also leave reviews and make payments.

---

### 🏠 Properties
- `id` (Primary Key)
- `owner_id` (Foreign Key to Users)
- `title`
- `location`
- `price_per_night`

**Relationship:** Each property is owned by a user and can have many bookings and reviews.

---

### 📅 Bookings
- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `check_in_date`
- `check_out_date`

**Relationship:** A booking is made by a user for a specific property.

---

### ✍️ Reviews
- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `rating`
- `comment`

**Relationship:** A user can leave a review for a property they’ve booked.

---

### 💳 Payments
- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `booking_id` (Foreign Key to Bookings)
- `amount`
- `payment_date`

**Relationship:** Each payment is tied to a user and a specific booking.

---

### Entity Relationships Summary:
- A **User** can:
  - own multiple **Properties**
  - make multiple **Bookings**
  - leave multiple **Reviews**
  - make multiple **Payments**

- A **Property**:
  - is owned by one **User**
  - can have many **Bookings**
  - can receive many **Reviews**

- A **Booking**:
  - is made by one **User**
  - is for one **Property**
  - can have one **Payment**

- A **Review**:
  - is written by one **User**
  - is about one **Property**

- A **Payment**:
  - is made by one **User**
  - corresponds to one **Booking**


## 🔐 API Security
To ensure secure access to the application:
- All API endpoints will implement proper authentication and authorization mechanisms.
- Sensitive data will be encrypted and protected using secure protocols (e.g., HTTPS).
- Rate-limiting and input validation will be used to prevent abuse and vulnerabilities.
- We will follow OWASP best practices for web API security.
## Team Roles

For the successful delivery of the AirBnB Clone project, the team members are assigned clear and collaborative roles inspired by software engineering best practices:

### 👨‍💻 Backend Developer
Responsible for building the core logic of the application using Python. This includes implementing routes, controllers, and handling requests/responses using the Flask framework.

### 🗃️ Database Administrator (DBA)
Ensures proper design, management, and optimization of the MySQL database. Handles schema creation, relationships, indexing, and ensures data integrity and security.

### 🌐 API Designer
Designs and documents RESTful API endpoints. Defines clear routes, response formats, and ensures the API adheres to standards for maintainability and usability.

### 🔐 DevOps/Security Lead
Implements version control (Git), manages deployment processes, and enforces security best practices like HTTPS, access control, and environment variable management.

### 🧪 QA/Test Engineer
Writes and executes unit and integration tests to ensure functionality, performance, and reliability. Automates testing where possible to ensure continuous quality.

### 📝 Documentation Lead
Maintains project documentation including the README, API documentation, and guides for setup, contribution, and testing.

### 🧭 Project Coordinator
Tracks progress, manages timelines, organizes meetings, and ensures team alignment with ALX project deliverables and deadlines.
Feature Breakdown
1. User Management
This feature allows users to register, log in, and manage their profiles. It includes user authentication and authorization to ensure secure access to the system.

2. Property Management
Hosts can list new properties, update existing ones, and manage availability. This feature enables the core functionality of showcasing homes for booking.

3. Booking System
Users can search for available properties based on filters like date and location, then make bookings. It ensures reservation handling, conflict checks, and availability updates.

4. Payment Integration
Handles payment processing for bookings through secure methods. This includes initiating, confirming, and tracking payments made by users.

5. Reviews and Ratings
Users can leave feedback and rate properties after their stay. This builds trust and transparency in the platform by helping future users make informed choices.

6. Admin Dashboard
Admins have access to user data, listings, and reports to monitor the platform's usage. It helps maintain platform quality, handle complaints, and resolve disputes.


## 👨‍💻 Team
Developed by Muwanuguzi Mark Miiro and team as part of the ALX SE Curriculum.


# projectpractice

👇

🚗 MechConnect Backend

Backend service for the MechConnect – Vehicle Service Booking Platform.
Built using Spring Boot 3 and Java 17, this REST API powers customer bookings, mechanic management, service packages, and order tracking.

🏗 Tech Stack

Java 17

Spring Boot 3

Spring Security

JWT Authentication

Spring Data JPA (Hibernate)

MySQL

Maven

📌 Features
🔐 Authentication & Authorization

Role-based access control (Admin, Customer, Mechanic)

JWT-based authentication

Secure REST APIs

👤 Customer Features

Register & Login

Search mechanics by location

Book services (Doorstep / Visit Workshop)

Track booking & order status

View booking history

🧑‍🔧 Mechanic Features

Mechanic registration

Manage services

Accept / Reject service requests

Update order progress

🛠 Admin Features

Manage users

Monitor bookings

Manage services & packages

Platform-level control

📂 Project Structure
src/main/java/com/mechconnect/backend
│
├── controller
├── service
├── repository
├── entity
│     └── enums
├── dto
├── config
└── MechConnectApplication.java
🗂 Database Entities

Admin

Customer

Mechanic

Booking

Orders

ServiceRequest

📑 Enums

OrderStatus

RequestStatus

ServiceMode

ServiceType

⚙️ Setup & Installation
1️⃣ Clone Repository
git clone https://github.com/your-username/mechconnect-backend.git
cd mechconnect-backend
2️⃣ Configure Database

Update src/main/resources/application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/mechconnect
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

Make sure MySQL is running and database mechconnect is created.

3️⃣ Run the Application

Using Maven:

mvn spring-boot:run

Or:

./mvnw spring-boot:run

Application runs at:

http://localhost:8080
🔐 Authentication (JWT)

After login, include token in request headers:

Authorization: Bearer <your-token>
📡 API Base URL
http://localhost:8080/api
🧪 Testing APIs

You can test APIs using:

Postman

Swagger (if configured)

cURL

Example:

curl -H "Authorization: Bearer <token>" http://localhost:8080/api/bookings
🔄 Order Lifecycle Flow

Customer creates booking

ServiceRequest generated

Mechanic accepts/rejects request

Order created

Order status updated (PENDING → IN_PROGRESS → COMPLETED)

🚀 Future Enhancements

Payment Integration

Notification Service (Email/SMS)

Docker Support

Production Deployment Guide

Logging & Monitoring

👨‍💻 Developer


Java Full Stack Developer

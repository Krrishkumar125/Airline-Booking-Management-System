# ✈️ Airline Management System — Microservices Architecture

A **modular, production-style backend system** for managing airline operations like flight search, user authentication, bookings, and reminders.

Built using:
**Node.js**, **Express.js**, **MySQL + Sequelize**, **RabbitMQ**, **JWT**, and **bcrypt**  
> 🧠 Designed to reflect real-world backend engineering with a clean microservices architecture.

---

## 📦 Microservices Breakdown

| Service | Description | GitHub Repo |
|--------|-------------|-------------|
| 🚪 **API Gateway** | Acts as the single entry point to route requests to all services | [API Gateway](https://github.com/Krrishkumar125/API_GATEWAY) |
| 🔐 **Auth Service** | Handles user registration, login, authentication using JWT + bcrypt | [Auth Service](https://github.com/Krrishkumar125/Auth_Service) |
| 🔍 **Flights & Search Service** | Lists flights and handles search by source/destination/date | [Flights & Search Service](https://github.com/Krrishkumar125/FlightsAndSearchService) |
| 📦 **Booking Service** | Books flights, manages seat availability and user bookings | [Booking Service](https://github.com/Krrishkumar125/AirTicketBookingService) |
| ⏰ **Reminder Service** | Sends booking reminders using RabbitMQ | [Reminder Service](https://github.com/Krrishkumar125/ReminderService) |

---

## 🛠️ Tech Stack

- **Node.js** + **Express.js**
- **MySQL** with **Sequelize ORM**
- **JWT** for secure authentication
- **bcrypt** for password hashing
- **RabbitMQ** for asynchronous communication in Reminder Service
- RESTful API Design
- Message Queue architecture for background job handling

---

## 🚀 How to Run the Project (Without Docker)

### ⚠️ Prerequisites
- Node.js (v16+)
- MySQL running locally
- RabbitMQ server running locally
- Postman or cURL for testing

---

### 🔌 1. Setup for Each Microservice

> Clone each microservice using the links above or use this pattern:

```bash
git clone https://github.com/KrrishKumar125/SERVICE_NAME
cd SERVICE_NAME
npm install
```

Set up a `.env` file inside each service with the following example:

```env
PORT=800X
DB_NAME=airline_service
DB_USER=root
DB_PASSWORD=your_password
DB_HOST=localhost
JWT_SECRET=your_jwt_secret
```

Then start the service:

```bash
npm start
```

Repeat this for each service:
- `API_GATEWAY`
- `AUTHSERVICE`
- `FLIGHTSANDSEARCHSERVICE`
- `BOOKINGSERVICE`
- `REMINDERSERVICE`

---

### 🧪 2. Testing the System

- All API calls go through the **API Gateway** at `http://localhost:3005`
- Use Postman collections or simple curl calls to test:

```bash
# Example login call
POST http://localhost:3005/auth/login
```

- The Reminder service runs in the background and consumes RabbitMQ messages to send reminders.

---

## 🔐 Authentication Flow (JWT + bcrypt)

- Signup → Password is hashed with **bcrypt**
- Login → Generates a **JWT token**
- Protected routes validate JWT in headers

---

## ✈️ Key Features

- ✅ Modular microservices — easy to maintain and scale
- ✅ MySQL + Sequelize — robust data management
- ✅ JWT + bcrypt — secure authentication
- ✅ RabbitMQ — efficient message queuing for reminders
- ✅ REST APIs for communication
- ✅ Ready for containerization and CI/CD

---

## 📁 Project Structure

```
airline-management-system/
├── README.md (This file)
🔗 API_GATEWAY 
🔗 AUTHSERVICE 
🔗 BOOKINGSERVICE 
🔗 FLIGHTSANDSEARCHSERVICE
🔗 REMINDERSERVICE
```

---

## 🔮 Future Improvements

- Docker + Docker Compose setup for easy orchestration
- Swagger API docs for each service
- Redis Caching for Flight Data
- Rate limiting, circuit breaking (via NGINX or Istio)
- CI/CD with GitHub Actions

---

## 🙋‍♂️ About Me

**Krrish Kumar**  
💻 Backend Developer | B.Tech CSE 
📍 Ghaziabad, India  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/krrishkumar125/)

---

## ⭐ If you found this interesting...

Please give a ⭐ to the repos — it motivates me to build more backend projects like this!
```

---

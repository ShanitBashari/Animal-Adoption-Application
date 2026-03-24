# 🐾 Pet Adoption Web Application

A full-stack web application for managing pet adoption listings and adoption requests.

Built as a final project using **React (frontend)** and **Spring Boot (backend)**, the system allows users to browse pets, publish animals, send adoption requests, and manage their activity.  
Includes an **admin panel** for managing users, categories, and animal approvals.

---

## 🧱 Tech Stack

**Frontend**
- React
- React Router DOM
- Material UI (MUI)

**Backend**
- Java 17 + Spring Boot
- Spring Security + JWT
- Spring Data JPA
- Maven

**Database**
- PostgreSQL

---

## ✨ Main Features

- Browse and search animals
- Add, edit, and manage personal listings
- Send and track adoption requests
- Approve/reject requests (owner side)
- Admin dashboard for managing users, categories, and animals
- Secure authentication with JWT

---

## 📄 Pages

- **Home** – browse and filter animals  
- **Animal Details** – full pet information + adoption action  
- **Add / Edit Animal** – create and manage listings  
- **My Listings** – manage user’s animals  
- **My Requests** – track sent adoption requests  
- **Requests for My Listings** – manage received requests  
- **Admin Dashboard** – system management  

---

## 🧠 Business Logic

- Users cannot adopt their own animals  
- Requests allowed only for available animals  
- No duplicate pending requests per user/animal  
- Approving a request:
  - marks animal as **ADOPTED**
  - rejects all other pending requests  
- Animals with existing requests are marked **INACTIVE** instead of deleted  
- New animals require admin approval  

---

## 🔐 Security

- JWT-based authentication  
- Role-based authorization  
- Protected API endpoints  
- Password hashing with BCrypt  

---

## 🗃️ Core Entities

- User  
- Animal  
- Category  
- AdoptionRequest  

## ▶️ Run the Application

### 1. Clone the repository
```bash
git clone <repo-url>
cd Pet-Adoption-Application
```

---

### 2. Run the backend (Spring Boot)
```bash
cd pet-adoption-server
mvn spring-boot:run
```

Backend runs on: **http://localhost:8080**

---

### 3. Run the frontend (React)
```bash
cd client
npm install
npm start
```

Frontend runs on: **http://localhost:3000**

---

## ⚙️ Environment Variables

### Frontend (`client/.env`)
Create a `.env` file inside the client folder:

```env
REACT_APP_API_URL=http://localhost:8080
```

---

### Backend (`application.properties`)
Configure your database connection:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/pet_adoption
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
```

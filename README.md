# 📓 JournalApp

A full-stack **Spring Boot + MongoDB + Redis** based journal application with **JWT authentication** and **Weather API integration**.  
Users can register, write personal journal entries, and get contextual insights like the current "feels like" weather temperature.

---

## 🚀 Features
- 🔐 **User Authentication** with JWT (Login/Register)  
- 📝 **Journal Management** – Create, update, delete journal entries  
- 🌦 **Weather Integration** – Fetches real-time weather info with Redis caching  
- ⚡ **Caching Layer** – Redis for faster weather API responses  
- 📚 **Swagger/OpenAPI UI** – Auto-generated API documentation  
- 🗄 **MongoDB** – Stores users and their journal entries  
- 🛡 **Spring Security** – Secures APIs with JWT filter  

---

## 🛠 Tech Stack
- **Backend:** Java 17, Spring Boot, Spring Security, Spring Data MongoDB  
- **Database:** MongoDB  
- **Cache:** Redis  
- **Auth:** JWT (JSON Web Token)  
- **API Docs:** Swagger (springdoc-openapi)  
- **Build Tool:** Maven  

---

## ⚙️ Setup & Run Locally

### 1. Prerequisites
- Java 17+
- Maven
- MongoDB running locally (`mongodb://localhost:27017`)
- Redis running locally (`redis://localhost:6379`)

### 2. Clone Repository
```bash
git clone https://github.com/sharmapiyu/journalApp.git
cd journalApp

3. Add Config

Open application.properties

Add your Weather API key:

weather.api.key=YOUR_API_KEY_HERE


Insert a config record in MongoDB:

{
  "key": "WEATHER_API",
  "value": "http://api.weatherstack.com/current?access_key=&query="
}

4. Run the app
mvn spring-boot:run

5. Open API docs

Go to:
👉 http://localhost:8080/swagger-ui/index.html

📌 API Endpoints
Auth

POST /auth/register – Register a new user

POST /auth/login – Login and get JWT

User

GET /user – Get greeting with weather info

PUT /user – Update user details

DELETE /user – Delete user

Journal

POST /journal – Create journal entry

GET /journal/{id} – Get a journal entry

GET /journal/all – Get all entries for a user

DELETE /journal/{id} – Delete entry

🔮 Improvements & Future Scope

Add sentiment analysis on journal entries

Replace @DBRef with userId reference for performance

Add Docker Compose for MongoDB + Redis

Implement role-based access control (RBAC)

👤 Author

Piyush Sharma

🌐 LinkedIn

💻 GitHub

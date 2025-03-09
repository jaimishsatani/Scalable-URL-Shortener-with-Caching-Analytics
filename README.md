# Scalable URL Shortener with Caching & Analytics

## 🚀 Overview
This project is a **high-performance URL shortener** built with the MERN stack, designed for **scalability and efficiency**. It allows users to shorten URLs, track analytics, and optimize performance using **Redis caching** and **MongoDB indexing**.

## ✨ Features
- 🔗 **Shorten Long URLs** – Convert long URLs into short, unique links.
- 📊 **Analytics Tracking** – Monitor clicks, referrers, and user locations.
- 🚀 **Fast Redirections** – Uses **Redis caching** for instant URL resolution.
- ⏳ **Expiration Mechanism** – Set custom expiration dates for short links.
- 🔒 **Secure Access** – JWT authentication for protected routes.
- 📏 **Rate Limiting** – Prevents spam and abuse using Redis.
- ⚡ **Scalability** – Optimized queries with **MongoDB indexing**.

## 🛠 Tech Stack
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (with indexing for fast retrieval)
- **Caching:** Redis (for quick access to recently accessed URLs)
- **Authentication:** JWT (JSON Web Tokens)
- **Deployment:** Docker, AWS (Optional for scalability)

## ⚙️ Installation & Setup
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-username/url-shortener.git
cd url-shortener
```

### 2️⃣ Install Dependencies
```sh
npm install
```

### 3️⃣ Configure Environment Variables
Create a `.env` file in the root directory and add:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
REDIS_HOST=localhost
REDIS_PORT=6379
```

### 4️⃣ Start the Server
```sh
npm start
```
The API will run on `http://localhost:5000`

## 🔥 API Endpoints
### 🔗 Shorten URL
```http
POST /api/url/shorten
```
**Request Body:**
```json
{
  "longUrl": "https://example.com"
}
```
**Response:**
```json
{
  "shortUrl": "http://short.ly/xyz123"
}
```

### 🎯 Redirect to Original URL
```http
GET /:shortCode
```
Redirects the user to the original URL.

### 📊 Get URL Analytics
```http
GET /api/url/stats/:shortCode
```
**Response:**
```json
{
  "clicks": 120,
  "referrers": ["google.com", "twitter.com"],
  "geoLocation": { "US": 80, "IN": 40 }
}
```

## 📌 Future Enhancements
- ✅ **Admin Dashboard** to manage URLs.
- ✅ **Custom URL Slugs** (user-defined short links).
- ✅ **Microservices Architecture** for improved scalability.

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

## 📜 License
This project is licensed under the MIT License.




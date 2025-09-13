# 🏙 ResolveOne – Backend

ResolveOne is a **dual-impact platform** enabling citizens to report civic issues (potholes, garbage, streetlights, etc.) and individuals to share personal struggles anonymously for timely support.  
This repository contains the **backend services** built using **Node.js + Express.js**, with **MongoDB** as the primary database.

---

## 🚀 Features

### Civic Issue Reporting
- API for reporting civic problems with **photo, geotag, and description**
- Automated **routing engine** assigns issues to relevant departments
- Status tracking & updates (submitted → acknowledged → resolved)
- Handles **multimedia uploads** (images, audio)

### Mental Health Support
- API for **anonymous post submission**
- 🤖 AI/NLP integration to detect severity or threat level
- Escalation & support **notifications via email/SMS**
- Community engagement endpoints (likes, comments, reactions)

### Shared Features
- Secure **RESTful APIs**  
- JWT-based authentication (for admins/staff)  
- Scalable, modular architecture  
- API-ready for **future mobile/web integrations**

---

## 🛠 Tech Stack

- **Node.js + Express.js** – Backend framework  
- **MongoDB + Mongoose** – NoSQL database  
- **AWS S3 / Firebase** – Media storage (images/audio)  
- **JWT + Bcrypt** – Authentication & security  
- **Python/NLP Service (Microservice)** – Threat detection & classification  
- **Multer** – File upload handling  
- **Nodemailer / Twilio** – Email & SMS notifications  
- **Docker** – Optional containerization for deployment  

---

## 📂 Project Structure

```

resolveone-backend/
│── src/
│   │── config/         # DB config, environment setup
│   │── controllers/    # Business logic
│   │── models/         # Mongoose schemas
│   │── routes/         # API route definitions
│   │── middlewares/    # Auth, error handling, validation
│   │── services/       # External services (email, SMS, AI)
│   │── utils/          # Helper functions
│   │── app.js          # Express app entry
│   │── server.js       # Server startup
│── uploads/            # Local uploads (dev only)
│── .env.example        # Environment variables template
│── package.json        # Dependencies & scripts

````

---

## ⚡ Installation & Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-username/resolveone-backend.git
   cd resolveone-backend
````

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Setup environment variables**
   Create a `.env` file in the root with:

   ```
   PORT=5000
   MONGO_URI=mongodb://localhost:27017/resolveone
   JWT_SECRET=your_secret_key
   CLOUD_STORAGE_KEY=your_cloud_key
   ```

4. **Run in development**

   ```bash
   npm run dev
   ```

5. **Run in production**

   ```bash
   npm start
   ```

---

## 🔗 API Endpoints (Sample)

### Civic Issues

* `POST /api/issues` – Create new civic issue
* `GET /api/issues` – Fetch all issues
* `GET /api/issues/:id` – Get single issue
* `PATCH /api/issues/:id` – Update issue status

### Mental Health

* `POST /api/posts` – Submit anonymous post
* `GET /api/posts` – Fetch community posts
* `POST /api/posts/flag` – Flag serious/urgent cases

### Admin

* `POST /api/admin/login` – Admin login
* `GET /api/admin/issues` – Manage civic reports
* `GET /api/admin/posts` – Manage anonymous posts

---

## 🤝 Team Members

* **Aman Prajapati (Leader)** – Coding, Producing, Pitch
* **Deepanshu** – Coding & Development
* **Harshit** – Testing & QA
* **Abhi Kumar** – Testing & QA
* **Dhruv Sangwan** – Project Management
* **Nancy** – Pitch & Communication

---

## 📜 License

This project is licensed under the **MIT License** – free to use, modify, and distribute.

---

## 🌟 Acknowledgments

* Built as part of a **Hackathon Project**
* Designed to empower communities through **civic engagement** and **mental well-being**
* Goal: **“No problem, big or small, should go unheard.”**

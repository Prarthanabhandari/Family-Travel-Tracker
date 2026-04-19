# 🌍 Family Travel Tracker

![Node.js](https://img.shields.io/badge/Node.js-Backend-green)
![Express](https://img.shields.io/badge/Express.js-Framework-black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![EJS](https://img.shields.io/badge/EJS-Templating-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 🌍 Overview

**Family Travel Tracker** is a full-stack web application that allows multiple users to track and visualize the countries they have visited.

---

## 🎯 Purpose of This Project

This project was created to:

- Learn **Node.js and Express.js**
- Practice **PostgreSQL database integration**
- Understand **multi-user data handling**
- Work with **dynamic UI rendering using EJS**
- Build a **real-world full-stack application**

---

## 🚀 Features

- 👨‍👩‍👧 Multi-user system  
- 🌍 Track visited countries  
- 🗺️ Interactive world map visualization  
- ➕ Add new countries dynamically  
- 🎨 Unique color per user  
- 📊 Total countries counter  
- 👤 Add new family members  

---

## 🛠️ Tech Stack

| Technology   | Usage              |
|-------------|-------------------|
| Node.js     | Backend runtime   |
| Express.js  | Server framework  |
| PostgreSQL  | Database          |
| EJS         | Templating engine |
| HTML/CSS    | Frontend UI       |

---

## 📂 Project Structure

```bash
Family-Travel-Tracker/
│
├── public/
│   └── styles/
│       └── main.css
│
├── views/
│   ├── index.ejs
│   └── new.ejs
│
├── index.js
├── package.json
├── package-lock.json
├── queries.sql
├── README.md
└── .gitignore
```

---

## 🎥 Demo Video

👉 Watch the project in action:

[![Watch Demo](https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)

> 📌 Replace `YOUR_VIDEO_ID` with your YouTube video ID

---

## 📸 Screenshots

### 🏠 Home Page
![Home Page](./screenshots/home.png)

### 👤 User Selection
![User Selection](./screenshots/user.png)

### 🌎 Add Country
![Add Country](./screenshots/add-country.png)

### 🗺️ Map View
![Map View](./screenshots/map.png)

### 📊 Statistics
![Stats](./screenshots/stats.png)

---

## 🚀 Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/Prarthanabhandari/Family-Travel-Tracker.git
cd Family-Travel-Tracker
```

---

### 2️⃣ Install Dependencies

```bash
npm install
npm install express body-parser ejs pg
npm install -g nodemon
```

---

### 3️⃣ Configure Project

Add this in `package.json`:

```json
"type": "module"
```

---

## 🗄️ Database Setup (PostgreSQL)

### Create Database

```sql
CREATE DATABASE country;
```

---

### Create Tables

```sql
CREATE TABLE users(
  id SERIAL PRIMARY KEY,
  name VARCHAR(15) UNIQUE NOT NULL,
  color VARCHAR(15)
);

CREATE TABLE visited_countries(
  id SERIAL PRIMARY KEY,
  country_code CHAR(2) NOT NULL,
  user_id INTEGER REFERENCES users(id)
);
```

---

### Insert Sample Data

```sql
INSERT INTO users (name, color)
VALUES 
('Angela', 'teal'),
('Jack', 'powderblue');

INSERT INTO visited_countries (country_code, user_id)
VALUES 
('FR', 1),
('GB', 1),
('CA', 2),
('FR', 2);
```

---

## ▶️ Run the Project

```bash
nodemon index.js
```

or

```bash
node index.js
```

Open in browser:

```
http://localhost:3000
```

---

## 🎮 How It Works

- 👤 Select a user  
- 🌎 Add a country name  
- 💾 Data stored in PostgreSQL  
- 🗺️ Map updates dynamically  
- 📊 Country count updates  
- 🔄 Switch between users  

---

## 👩‍💻 Author

**Prarthana Bhandari**

---

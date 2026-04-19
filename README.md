# 🌍 Family Travel Tracker

![Node.js](https://img.shields.io/badge/Node.js-Backend-green)
![Express](https://img.shields.io/badge/Express.js-Framework-black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![EJS](https://img.shields.io/badge/EJS-Templating-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 🌍 Overview

**Family Travel Tracker** is a full-stack web application that allows multiple users to track and visualize the countries they have visited.

Each user can:
- Add visited countries  
- View their travel map  
- Track total visited locations  

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

| Technology | Usage |
|----------|------|
| Node.js | Backend runtime |
| Express.js | Server framework |
| PostgreSQL | Database |
| EJS | Templating engine |
| HTML/CSS | Frontend UI |

---

## 📂 Project Structure

Family-Travel-Tracker/
│── public/
│ ├── styles/
│ │ └── main.css
│── views/
│ ├── index.ejs
│ └── new.ejs
│── index.js
│── package.json
│── package-lock.json
│── queries.sql
│── README.md
│── .gitignore



---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/Prarthanabhandari/Family-Travel-Tracker.git

### Install Dependencies

```bash
npm install

npm install express body-parser ejs pg

npm install -g nodemon

Add this in package.json:
"type": "module"

🗄️ Database Setup (PostgreSQL)
Create Database
CREATE DATABASE country;
Create Tables
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
Insert Sample Data
INSERT INTO users (name, color)
VALUES ('Angela', 'teal'), ('Jack', 'powderblue');

INSERT INTO visited_countries (country_code, user_id)
VALUES ('FR', 1), ('GB', 1), ('CA', 2), ('FR', 2 );


### Run The Project

```bash

nodemon index.js

node index.js

http://localhost:3000


🎮 How It Works
Select a user
Add a country name
Country gets added to database
Map updates dynamically
Total visited countries count updates
Switch between users



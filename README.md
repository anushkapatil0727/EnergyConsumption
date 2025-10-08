# ⚡ Smart Home Energy Management System (SHEMS)

This project is a **Flask-based Energy Consumption Tracking and Visualization Platform** that helps users **monitor, analyze, and compare their energy usage** over various time periods — daily, hourly, monthly, and yearly.  
It combines an intuitive front-end built with **HTML, CSS, and Chart.js** with a **MySQL-backed Flask API** to deliver a seamless and insightful experience.

---

## 🧩 Project Overview

The Smart Home Energy Management System (SHEMS) allows users to:
- Track their **energy consumption** and **energy prices** across multiple time frames.
- Visualize real-time analytics using **interactive charts**.
- Log in securely and analyze personalized usage insights.
- Support **location-based** tracking and data-driven optimization.

---

## 🏗️ Project Structure

```bash
SHEMS/
│
├── app.py                           # Flask backend with all route endpoints
├── SQLFile.sql                      # MySQL schema and database initialization
│
├── templates/
│   ├── index.html                   # Landing page with login detection
│   ├── login.html                   # User login form
│   ├── signup.html                  # User registration page
│   │
│   ├── dailyEnergyConsumption.html  # Daily consumption graph (Chart.js)
│   ├── totalEnergyConsumption.html  # Total consumption graph
│   ├── hourlyEnergyPriceChange.html # Hourly price fluctuation graph
│   ├── energyPrices.html            # Daily energy price trend graph
│   └── yearlyEnergyConsumption.html # Yearly consumption overview
│
└── static/
    └── (optional) CSS / JS assets if extended
💡 Key Features
🔐 User Authentication
Secure user sign-up and login using Flask sessions

Form validation for credentials and user data

📊 Real-Time Data Visualization
Interactive visualizations powered by Chart.js

Track and compare energy usage across:

Hourly → hourlyEnergyPriceChange.html

Daily → dailyEnergyConsumption.html

Total → totalEnergyConsumption.html

Yearly → yearlyEnergyConsumption.html

🌍 Location-Based Analytics
Each visualization is linked to a unique location_id

Dynamic routing handled by Flask’s url_for()

📈 Flask API Integration
Backend provides JSON responses with labels and values

Frontend fetch() calls update graphs in real time

💾 MySQL Integration
Centralized schema (SQLFile.sql) for users, locations, and energy data

Optimized for large-scale energy datasets

🧰 Tech Stack
Component	Tools / Libraries
Frontend	HTML5, CSS3, JavaScript, Chart.js
Backend	Flask (Python)
Database	MySQL
Visualization	Chart.js
Server	Flask Development Server
Version Control	Git & GitHub

🧠 Key Insights & Learnings
Showcases end-to-end full-stack integration from UI → API → Database → Visualization

Leverages Jinja2 templating for dynamic data flow

Demonstrates a modular and scalable backend structure

Can be easily extended for IoT data, real-time analytics, and machine learning forecasting

🚀 How to Run
1️⃣ Clone the Repository
bash
Copy code
git clone https://github.com/yourusername/SHEMS.git
cd SHEMS
2️⃣ Set Up the Environment
bash
Copy code
python3 -m venv venv
source venv/bin/activate     # On Mac/Linux
venv\Scripts\activate        # On Windows

pip install flask mysql-connector-python
3️⃣ Configure MySQL
Start your MySQL server

Create a database:

sql
Copy code
CREATE DATABASE SHEMS;
Import the schema:

bash
Copy code
mysql -u root -p SHEMS < SQLFile.sql
Update your credentials in app.py:

python
Copy code
connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="yourpassword",
    database="SHEMS"
)
4️⃣ Run the Flask App
bash
Copy code
python app.py
App will run at:
👉 http://127.0.0.1:5000

🗂️ Repository Contents
File	Description
app.py	Flask backend with all endpoints
SQLFile.sql	MySQL database schema and setup
index.html	Landing page with login detection
login.html / signup.html	Authentication templates
dailyEnergyConsumption.html	Daily consumption graph
totalEnergyConsumption.html	Total energy consumption
hourlyEnergyPriceChange.html	Hourly price fluctuation visualization
energyPrices.html	Daily energy price trend visualization
yearlyEnergyConsumption.html	Yearly overview visualization

🧭 Future Enhancements
📡 IoT Smart Meter Integration

⚙️ Real-time MQTT Data Streaming

🧮 Predictive Analytics for Energy Forecasting

🖥️ Admin Dashboard for Usage Insights

☁️ Cloud Deployment (AWS, Render, or Railway)

👩‍💻 Author
Anushka Patil

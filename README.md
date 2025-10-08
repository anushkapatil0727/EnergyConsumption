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

## 💡 Key Features

### 🔐 User Authentication
- Secure user sign-up and login using **Flask sessions**  
- Form validation for credentials and user data  

### 📊 Real-Time Data Visualization
- Interactive graphs powered by **Chart.js**  
- Tracks energy consumption and prices across:
  - **Hourly** → `hourlyEnergyPriceChange.html`
  - **Daily** → `dailyEnergyConsumption.html`
  - **Total** → `totalEnergyConsumption.html`
  - **Yearly** → `yearlyEnergyConsumption.html`

### 🌍 Location-Based Analytics
- Each visualization is linked to a specific **location_id**
- Dynamic route handling with Flask’s `url_for()`

### 📈 Data from Backend (Flask API)
- `fetch()` POST requests send `location_id` and `selected_date` to Flask routes  
- Flask returns JSON responses with `labels` and `values` for plotting

### 💾 MySQL Integration
- Centralized schema (`SQLFile.sql`) for user, location, and energy tables  
- Designed for scalable data ingestion and analysis  

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-------------|
| **Frontend** | HTML5, CSS3, JavaScript (Chart.js) |
| **Backend** | Python Flask |
| **Database** | MySQL |
| **Visualization** | Chart.js |
| **Server** | Flask’s built-in development server |
| **Version Control** | Git / GitHub |

---

## 🧠 Key Insights & Learnings

- Demonstrates **full-stack integration** from UI → backend → database → visualization  
- Uses **Flask’s Jinja2 templating** to pass `location_id` and `selected_date` seamlessly  
- Each visualization script fetches live data from backend APIs, emphasizing **data-driven design**  
- The system structure makes it easy to extend with **machine learning** or **IoT integrations** (e.g., real sensor data or energy optimization models)  

---

## ⚙️ How to Run the Project

### 1️⃣ Clone the Repository
```bash
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
Start your MySQL server.

Create the database:

sql
Copy code
CREATE DATABASE SHEMS;
Import the schema:

bash
Copy code
mysql -u root -p SHEMS < SQLFile.sql
Update your connection details in app.py:

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
By default, Flask runs on:

cpp
Copy code
http://127.0.0.1:5000
🗂️ Repository Contents Summary
File	Description
app.py	Flask backend with API routes for login, signup, and visualization
SQLFile.sql	MySQL database schema and setup
index.html	Entry page with login state
login.html / signup.html	User authentication pages
dailyEnergyConsumption.html	Daily energy consumption visualization
totalEnergyConsumption.html	Total daily energy overview
hourlyEnergyPriceChange.html	Hourly energy price fluctuation
energyPrices.html	Daily price trends
yearlyEnergyConsumption.html	Multi-year trend visualization

🚀 Future Enhancements
Integration with IoT smart meters

Real-time MQTT data ingestion

Predictive analytics for consumption forecasting

Admin dashboard for aggregated insights

Cloud deployment on AWS / Render / Railway

👩‍💻 Author
Anushka Patil

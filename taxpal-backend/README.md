# 🚀 TaxPal Backend

The **TaxPal Backend** provides the REST APIs and server-side functionality for the TaxPal – Personal Finance & Tax Estimator for freelancer.

---

✨ Backend Features
🔐 User Registration & Login
🔑 JWT-based Authentication
💰 Transaction Management
📊 Dashboard Summary & Analytics
💵 Budget Management
🏷️ Category Management
🧮 Tax Estimation
📄 Financial Report Generation
🔔 Alerts Management
🗄️ MySQL Database Integration using Sequelize

## 🛠️ Tech Stack

* **Runtime:** Node.js
* **Framework:** Express.js
* **Database:** MySQL 8.0
* **ORM:** Sequelize
* **Authentication:** JWT
* **Password Security:** bcryptjs
* **Report Generation:** PDFKit

---

## 📋 Prerequisites

Before running the backend, make sure the following are installed:

1. **Node.js** (v16 or higher)
2. **MySQL Server 8.0** or **XAMPP / WAMP**

---

## 🛠️ Step-by-Step Setup Guide

### Step 1: Install Dependencies

Open the terminal in the `taxpal-backend` directory and run:

```bash
npm install
```

### Step 2: Configure Environment Variables

Create a `.env` file inside the `taxpal-backend/` directory:

```env
PORT=5000
DB_HOST=127.0.0.1
DB_PORT=3306
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=taxpal
DB_DIALECT=mysql
JWT_SECRET=your_jwt_secret_key_here
```

### Step 3: Run the Server (Automatic Database & Table Creation)

The backend automatically connects to MySQL, creates the `taxpal` database if required, and synchronizes the required tables using Sequelize ORM.

Start the server:

```bash
node src/server.js
```

**Expected Terminal Output:**

```text
✅ MySQL connected successfully via Sequelize
✅ MySQL models & tables synchronized successfully
Server running on port 5000
```

---

## 📂 Project API Base URL & Endpoints

Base URL:  http://localhost:5000/api
Auth: /api/auth/register, /api/auth/login
Transactions: /api/transactions
Budgets: /api/budgets
Categories: /api/categories
Dashboard: /api/dashboard/summary, /api/dashboard/analytics
Tax Estimate: /api/tax
Reports: /api/reports/transactions, /api/reports/tax, /api/reports/dashboard
Alerts: /api/alerts

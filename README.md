# 🌾 MandiConnect API Testing

![Postman](https://img.shields.io/badge/Tested%20With-Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![API Testing](https://img.shields.io/badge/Type-API%20Testing-0052CC?style=for-the-badge&logo=swagger&logoColor=white)
![REST API](https://img.shields.io/badge/Protocol-REST%20API-00C853?style=for-the-badge&logo=fastapi&logoColor=white)
![Beginner Friendly](https://img.shields.io/badge/Level-Beginner%20Friendly-FFD600?style=for-the-badge&logo=bookstack&logoColor=black)
![JSON](https://img.shields.io/badge/Format-JSON-lightgrey?style=for-the-badge&logo=json&logoColor=black)

> A hands-on API testing project for **MandiConnect** — a platform connecting farmers and buyers in agricultural markets. This project focuses on validating backend REST APIs using Postman, ensuring correct responses, status codes, and data integrity.

---

## 📌 Overview

**MandiConnect** is an agricultural marketplace platform that enables farmers to list their produce and buyers to place orders through a digital interface. This project covers end-to-end **manual API testing** of the platform's backend services.

The goal of this project is to:
- Verify that all API endpoints return the correct responses
- Validate request/response structure and data formats
- Identify bugs and inconsistencies in the backend behavior
- Document test results and edge cases clearly

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| 🟠 **Postman** | API testing and collection management |
| 🌐 **REST API** | Architecture style of the tested APIs |
| 📄 **JSON** | Request body and response data format |
| 📋 **Excel / Notion** | Test case documentation |
| 🔗 **HTTP Methods** | GET, POST, PUT, DELETE |

---

## 🔌 APIs Tested

| # | API Name | Method | Endpoint | Description |
|---|----------|--------|----------|-------------|
| 1 | User Registration | `POST` | `/api/auth/register` | Register a new user (farmer/buyer) |
| 2 | User Login | `POST` | `/api/auth/login` | Authenticate user and receive token |
| 3 | Get All Listings | `GET` | `/api/listings` | Fetch all available produce listings |
| 4 | Create Listing | `POST` | `/api/listings/create` | Add a new produce listing |
| 5 | Update Listing | `PUT` | `/api/listings/:id` | Update an existing listing |
| 6 | Delete Listing | `DELETE` | `/api/listings/:id` | Remove a listing |
| 7 | Place Order | `POST` | `/api/orders/place` | Buyer places an order |
| 8 | Get Order Status | `GET` | `/api/orders/:id` | Fetch current order status |
| 9 | User Profile | `GET` | `/api/user/profile` | Retrieve logged-in user details |
| 10 | Logout | `POST` | `/api/auth/logout` | Invalidate user session/token |

---

## 🧪 Testing Scenarios

### ✅ Positive Test Cases
- Successful user registration with valid credentials
- Login with correct username and password returns a valid token
- Fetching listings returns a non-empty list with correct data
- Creating a listing with all required fields returns `201 Created`
- Placing a valid order returns an order confirmation with ID

### ❌ Negative Test Cases
- Login with wrong password returns `401 Unauthorized`
- Registration with duplicate email returns proper error message
- Creating a listing without required fields returns `400 Bad Request`
- Accessing protected routes without token returns `403 Forbidden`
- Passing invalid ID to GET order returns `404 Not Found`

### ⚠️ Edge Cases
- Empty string in required fields
- Extremely long input values in name/description fields
- Special characters in search parameters
- Expired or malformed JWT tokens

---

## ✔️ Validations Performed

- 🔢 **Status Code Validation** — Verified correct HTTP status codes (200, 201, 400, 401, 403, 404, 500)
- 📦 **Response Body Validation** — Checked response fields, data types, and values
- ⏱️ **Response Time Check** — Ensured APIs respond within acceptable time limits
- 🔐 **Authentication Validation** — Verified token-based access control
- 📋 **Schema Validation** — Confirmed response structure matches expected JSON schema
- 🔁 **CRUD Operation Validation** — Tested all Create, Read, Update, Delete flows
- 🚫 **Error Message Validation** — Ensured meaningful error messages are returned

---

## 📸 Screenshots

### 🔐 Login API — Success Response
![Login API](./screenshots/login_success.png)

### 🚫 Login API — Invalid Credentials
![Login Failed](./screenshots/login_failed.png)

### 📋 Get All Listings — Response
![Get Listings](./screenshots/get_listings.png)

### ➕ Create Listing — Request & Response
![Create Listing](./screenshots/create_listing.png)

### 🛒 Place Order — Success
![Place Order](./screenshots/place_order.png)

### ❌ Unauthorized Access — 403 Error
![Unauthorized](./screenshots/unauthorized_access.png)

> 📁 All screenshots are stored in the `/screenshots` folder of this repository.

---

## 📁 Project Structure

```
MandiConnect-API-Testing/
│
├── 📂 postman/
│   ├── MandiConnect_Collection.json       # Postman collection (exported)
│   └── MandiConnect_Environment.json      # Environment variables
│
├── 📂 screenshots/
│   ├── login_success.png
│   ├── login_failed.png
│   ├── get_listings.png
│   ├── create_listing.png
│   ├── place_order.png
│   └── unauthorized_access.png
│
├── 📂 test-cases/
│   └── MandiConnect_TestCases.xlsx        # Detailed test case sheet
│
├── 📂 bug-reports/
│   └── Bug_Report_MandiConnect.xlsx       # Logged bugs and issues
│
└── 📄 README.md                           # Project documentation
```

---

## 🔗 Postman Collection

You can import the Postman collection directly to explore and run all test cases:

[![Run in Postman](https://run.pstmn.io/button.svg)](https://www.postman.com/)

> 📥 **To import manually:**
> 1. Open Postman
> 2. Click **Import**
> 3. Select `postman/MandiConnect_Collection.json`
> 4. Set up the environment using `MandiConnect_Environment.json`
> 5. Run the collection using **Collection Runner**

---

## 💡 Key Learnings

Through this project, I gained practical experience in:

- 🧠 Understanding how REST APIs work (request, response, headers, body)
- 🔐 Learning about token-based authentication (Bearer Token / JWT)
- 🧪 Writing structured test cases for manual API testing
- 🛠️ Using Postman features like Collections, Environments, and Pre-request Scripts
- 📋 Documenting bugs clearly with steps to reproduce
- 🔍 Identifying edge cases and boundary conditions in APIs
- ✅ Validating API responses against expected behavior

---

## 👤 Author

**Shweta Deore**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/your-profile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/your-username)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your-email@gmail.com)

---

<div align="center">

⭐ If you found this project useful, consider giving it a **star**!

*Made with ❤️ for learning and growth in Software Testing*

</div>

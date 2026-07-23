# User Management API Testing

## Project Overview

This project demonstrates functional API testing of a User Management REST API using **Postman** and **JSON Server**. It includes CRUD operations, automated test scripts, positive and negative test scenarios, environment variables, and Collection Runner execution.

---

## Tools Used

- Postman
- JSON Server
- JavaScript (Postman Test Scripts)
- REST API
- GitHub

---

## API Methods Tested

| Method | Description |
|---------|-------------|
| GET | Retrieve all users and a specific user |
| POST | Create a new user |
| PUT | Update complete user details |
| PATCH | Update user email |
| DELETE | Delete a user |

---

## Test Scenarios

### Positive Test Cases

- Get all users
- Get user by ID
- Create a new user
- Update user details
- Update user email
- Delete a user

### Negative Test Cases

- Get a non-existing user
- Create a user without the required **name** field
- Create a user with an invalid email format

---

## Automated Test Scripts

Automated assertions were added to verify:

- HTTP status codes
- Response body
- User details
- Successful creation and update of users
- Error responses for invalid requests

Example:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

---

## Environment Variable

Environment Name:

```
User Management API Environment
```

Variable:

```
base_url = http://localhost:3000
```

Requests use:

```
{{base_url}}/users
```

---

## Collection Runner

The entire collection was executed using **Postman Collection Runner**.

### Results

- Total Automated Assertions: 15
- Passed: 15
- Failed: 0
- Pass Rate: 100%

---

## Project Files

```
User Management API Testing
│
├── README.md
├── db.json
├── User_Management_API_Test_Cases.xlsx
├── User_Management_API_Test_Execution_Report.xlsx
```

---

## Key Observations

Since JSON Server is a mock API, it does not perform server-side validation for required fields or email format.

Examples:

- Creating a user without a name returned **201 Created**
- Creating a user with an invalid email returned **201 Created**

In a production API, these requests would typically return **400 Bad Request**.

---

## Learning Outcomes

Through this project, I gained practical experience in:

- REST API Testing
- CRUD API Operations
- Postman Collections
- Environment Variables
- JavaScript Test Scripts
- Positive & Negative Testing
- Collection Runner
- API Test Documentation
- GitHub Project Management

1) Design a proper database to support the user stories.

CREATE TABLE Employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(255) UNIQUE NOT NULL,
    name VARCHAR(50) NOT NULL,
    company VARCHAR(255) NOT NULL,
    credit_balance DECIMAL(10, 2) DEFAULT 1000.00
);

2)	Design and implement APIs.

1) POST request
URL: http://127.0.0.1:8080/employees
request body:
{ 
        "email": "rameshkumar@gmail.com",
        "name": "ramesh kumar",
        "company": "RK Group",
        "creditBalance": 3000.00
}
Response:
{
    "success": true,
    "credit": 3000.00
}

2) GET request for fetching all records
URL: http://127.0.0.1:8080/employees
Response:
[
    {
        "id": 1,
        "email": "kumar.rajesh@gmail.com",
        "name": "Rajesh",
        "company": "R Group",
        "creditBalance": 1000.00
    },
    {
        "id": 2,
        "email": "kumar.ravi@gmail.com",
        "name": "Ravi",
        "company": "Raj Group",
        "creditBalance": 1000.00
    }
]

GET : fetching balance by email
URL: http://127.0.0.1:8080/employees/balance?email=test4@company1.com
Response:
{
    "credit": 2500.00
}

PUT : Update balance by email
URL: http://127.0.0.1:8080/employees
{ 
        "email": "kumar@gmail.com",
        "creditBalance": 4000.00

}
Response:
{
    "success": true,
    "new_credit": 4000.00
}

3) Design a simple frontend to view employee credit balance.
Code has been designed for BankEnd and used technologies Java with SpringBoot framework.

  

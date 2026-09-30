# Employee REST API

A beginner-friendly Spring Boot REST API demonstrating Controller -> Service flow.

## Requirements
- Java 17+
- Maven 3.9+ (or use the Maven wrapper if added by your IDE)
- IntelliJ IDEA / STS / Eclipse

## Run
1. Import this folder as a Maven project.
2. Run `EmployeeRestApiApplication`.
3. The application starts on port 8080.

## APIs

### Get all employees
GET http://localhost:8080/employees

### Get employee
GET http://localhost:8080/employees/101

### Create employee
POST http://localhost:8080/employees
Content-Type: application/json

{
  "name": "Alice",
  "department": "Finance",
  "salary": 80000
}

### Update employee
PUT http://localhost:8080/employees/101
Content-Type: application/json

{
  "name": "John Updated",
  "department": "Engineering",
  "salary": 85000
}

### Delete employee
DELETE http://localhost:8080/employees/101

## Important
This first version stores data in memory, so restarting the application resets the employees.

Teaching flow:
Client/Postman -> Controller -> Service -> in-memory List -> Response

Next step can be adding Repository + JPA + MySQL.

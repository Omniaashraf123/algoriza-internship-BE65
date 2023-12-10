# algoriza-internship-BE65
vezeeta endpoint
backend

# Prerequisites

###### 1- [.NET 5.0](https://dotnet.microsoft.com/en-us/download/dotnet/5.0)
###### 2- [SQL-Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
###### 3- [SSMS](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)



# To Start

### 1. make changes in DefaultConnection of ` appsettings.json `

```json
  "ConnectionStrings": {
    "DefaultConnection": "server=WINDOWS11\\SQLEXPRESS;database=Backend;trusted_connection=true;"
  },
```
### 2. For Database connection

## Build the solution
```
dotnet ef migrations add InitialCreate --context DataContext --output-dir Migrations
```
```
dotnet ef database update
```
```
dotnet run
```
### 3. Use postman or thunderclient further

###### i. POST method
```
(https://localhost:5001/api/authenticate)
```
 There in basic auth use these credentials

-  **UserName:** admin@gmail.com
-  **Password:** Passcode1

#### Token would be generated:

#### Screenshots
<div>
<img src="https://github.com/Omniaashraf123/algoriza-internship-BE65/assets/85138012/4f2765c0-9777-453b-b4c2-5c00337b1f51" width="150">
<img src="https://github.com/Omniaashraf123/algoriza-internship-BE65/assets/85138012/0d7d6999-9813-42c3-87f6-66846c39b18c" width="150">
</div>

# thunderclient Log

### 1. POST login
```
(https://localhost:5001/api/authenticate)
```
### 2. GET all_users
```
(https://localhost:5001/api/authenticate)
```
### 3. GET first_user
```
(https://localhost:5001/api/administration/1)
```
### 4. POST create_user
```
(https://localhost:5001/api/authenticate)
```
### 5. DELETE first_user
```
(https://localhost:5001/api/authenticate/1)
```
-----------------------------------------------

### 1. GET all_drugs
```
(https://localhost:5001/api/drugs/)
```
### 2. GET drugs_by_id
```
(https://localhost:5001/api/drugs/id-1)
```
### 3. GET drugs_by_name
```
(https://localhost:5001/api/drugs/name-sinarest)
```
### 4. POST drugs
```
(https://localhost:5001/api/drugs/)
```
```json
{
  "name": "sinarest",
  "manufacturer": "adv pharma",
  "manufacturedDate": "2022-01-01T06:30:00",
  "expiryDate": "2022-11-01T00:00:00",
  "quantities": 250,
  "location": "pune",
  "userId":1
}
```
-----------------------------------------------

### 1. GET all_orders_by_order
```
(https://localhost:5001/api/order/order)
```
### 2. GET all_orders_by_drug
```
(https://localhost:5001/api/order/drug)
```
-----------------------------------------------

### 1. POST order
```
(https://localhost:5001/api/products/1)
```
``` json
{
  "MemberId":"2434",
  "Insurance_Policy_Number": "123456789",
  "InsuranceProvider": "ICICI",
  "PrescriptionDate": "1999-11-18T06:30:00",
  "DosageForDay": 2,
  "PrescriptionCourse": "2 weeks",
  "DoctorDetails": "Dr. John",
  "UserId":"1",
  "DrugId":"1"
}
```
-----------------------------------------------

### 1. GET all_messages
```
(https://localhost:5001/api/contactus/)
```
-----------------------------------------------

### 1. GET first_messages
```
(https://localhost:5001/api/contactus/1)
```

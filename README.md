# Cloud Computing Lab 5

## Student Details
- Name: Rohit Raina
- Lab: Cloud Computing Lab 5

## Assignment 1: AWS RDS PostgreSQL

### Objective
Deploy PostgreSQL on Amazon RDS and connect the existing Drupal application running on EC2 to the RDS database.

### AWS Resources
- EC2 Instance: Rohit-Drupal-Lab4
- EC2 Region: eu-north-1
- RDS Instance: rohit-drupal-lab5-pg
- Database Engine: PostgreSQL
- RDS Instance Class: db.t4g.micro
- Database Name: drupal
- Database User: drupaluser
- RDS Port: 5432

### RDS Security
RDS PostgreSQL inbound access is restricted to the EC2 security group.
Public access to the RDS instance is disabled.

### Drupal-RDS Connection
Drupal 11.4.7 successfully connects to the RDS PostgreSQL database.

Evidence:
- `Lab5_RDS_Drupal_Connection.png`

### CRUD Operations
CRUD operations were demonstrated through the running Drupal application.

- Create: Node created successfully
- Read: Node title and published status verified
- Update: Node title updated successfully
- Delete: Node deleted successfully
- Verification: Deleted node confirmed absent

Evidence:
- `Lab5_Final_CRUD_and_App.png`

### Drupal Application
The Drupal application is running on the EC2 instance and returns HTTP 200.

Application URL:
http://13.60.27.33

Evidence:
- `Lab5_Drupal_App_Running.png`

---

## Assignment 2: Amazon DynamoDB

### Objective
Deploy and use DynamoDB with the EC2 application using IAM role-based access.

### DynamoDB Configuration
- Table Name: Lab5DrupalNoSQL
- Region: eu-north-1
- Capacity Mode: On-Demand
- Partition Key: id
- Sort Key: String

### DynamoDB Data Types
The implementation demonstrates the required DynamoDB data types:

- String (S)
- Number (N)
- Boolean (BOOL)
- List (L)
- Map (M)

Evidence:
- `Lab5_DynamoDB_5_Datatypes.png`

### DynamoDB CRUD
The following operations were demonstrated:

- Create
- Read
- Update
- Delete

Evidence:
- `Lab5_DynamoDB_CRUD_Read.png`
- `Lab5_DynamoDB_CRUD_Update.png`
- `Lab5_DynamoDB_CRUD_Delete.png`

### IAM Security
DynamoDB access is provided through the EC2 IAM role instead of hardcoded AWS access keys.

IAM Role:
`DrupalLab5SecretsRole`

Evidence:
- `Lab5_DynamoDB_IAM_Policy.png`
- `Lab5_DynamoDB_EC2_IAM_Role.png`

## Submission Evidence

The screenshots demonstrate:
1. EC2 Drupal application running
2. Drupal connected to RDS PostgreSQL
3. RDS CRUD operations
4. DynamoDB five required data types
5. DynamoDB CRUD operations
6. EC2 IAM role and DynamoDB permissions
7. Restricted RDS security-group access

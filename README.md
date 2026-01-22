# Serverless Bus Tracking System

## Description
This project implements a real-time bus tracking system using a serverless architecture on AWS. The system tracks bus locations, stores data efficiently, and provides real-time updates to users without managing any servers.

---

## Technologies Used
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- HTML, CSS, JavaScript (Frontend)
- AWS IAM
- CloudWatch (Logging & Monitoring)

---

## Architecture Overview
- Frontend sends bus location and tracking requests
- API Gateway exposes REST APIs
- Lambda functions process incoming requests
- DynamoDB stores and retrieves bus tracking data
- Fully serverless architecture with automatic scaling

---

## Project Workflow
1. Bus location data is sent to the backend through API Gateway
2. API Gateway triggers AWS Lambda functions
3. Lambda processes the request and updates DynamoDB
4. DynamoDB stores real-time bus tracking information
5. Lambda returns the response to the frontend
6. Users view live bus tracking data

---

## Implementation Steps

### Step 1: Create DynamoDB Table
- Created a DynamoDB table to store bus details
- Used partition key (BusID / RouteID)
- Enabled on-demand capacity for automatic scaling

### Step 2: Create Lambda Functions
- Created Lambda functions to:
  - Update bus location
  - Fetch bus location
- Added required IAM permissions for DynamoDB access

### Step 3: Configure API Gateway
- Created REST APIs for bus tracking
- Integrated API Gateway with Lambda functions
- Enabled CORS for frontend access

### Step 4: IAM Role Configuration
- Created IAM roles with least privilege access
- Attached roles to Lambda functions

### Step 5: Frontend Integration
- Frontend sends HTTP requests to API Gateway endpoints
- Displays real-time bus location data to users

---

## Validation
- Successfully stored and retrieved bus data from DynamoDB
- Verified Lambda execution using CloudWatch logs
- Tested APIs using browser and API testing tools
- Confirmed automatic scaling without server management

---

## Outcome
- Fully serverless bus tracking application
- Real-time data handling with low latency
- Automatic scaling and high availability
- No server provisioning or maintenance required

---

## Key Learnings
- Designing serverless applications on AWS
- Integrating API Gateway with Lambda
- Using DynamoDB for real-time NoSQL data
- Implementing secure access using IAM roles
- Building scalable and cost-effective cloud solutions

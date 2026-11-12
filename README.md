# AWS Serverless Three-Tier Web Application

## Project Overview

Designed and deployed a serverless three-tier web application on Amazon Web Services (AWS) using S3, CloudFront, API Gateway, Lambda, and DynamoDB.

The application demonstrates how frontend, business logic, and database layers can work together without managing servers, resulting in a scalable, cost-effective, and highly available architecture.

---

# Architecture

## Three-Tier Design

### Presentation Tier
- Amazon S3
- Amazon CloudFront

### Logic Tier
- AWS Lambda
- Amazon API Gateway

### Data Tier
- Amazon DynamoDB

### Architecture Flow

```text
User
 │
 ▼
CloudFront
 │
 ▼
S3 Static Website
 │
 ▼
API Gateway
 │
 ▼
Lambda Function
 │
 ▼
DynamoDB
```

---

# AWS Services Used

| Service | Purpose |
|----------|----------|
| S3 | Static website hosting |
| CloudFront | Global content delivery |
| API Gateway | REST API endpoint |
| Lambda | Backend application logic |
| DynamoDB | NoSQL database |
| IAM | Service permissions |

---

# Features

- Serverless architecture
- Global content delivery
- Dynamic data retrieval
- REST API integration
- NoSQL database storage
- Scalable backend services
- Low operational overhead

---

# Implementation Steps

## Presentation Tier

Hosted frontend files in an Amazon S3 bucket and distributed content globally through CloudFront.

### Responsibilities

- Host HTML, CSS and JavaScript files
- Deliver content through CDN
- Improve website performance

---

## Logic Tier

Created a Lambda function and connected it with API Gateway.

### Responsibilities

- Process user requests
- Retrieve data from DynamoDB
- Return JSON responses

---

## Data Tier

Created a DynamoDB table using:

```text
Partition Key: userId
```

### Responsibilities

- Store user records
- Provide fast lookups
- Support serverless backend queries

---

# Challenges Faced

## API Integration Issues

While integrating the frontend and backend services, the initial fetch requests failed because the API Gateway endpoint was not configured correctly.

### Solution

- Verified API Gateway endpoint
- Updated frontend JavaScript
- Reuploaded application files to S3

---

## CORS Errors

Browser requests were blocked due to Cross-Origin Resource Sharing (CORS) restrictions between CloudFront-hosted frontend resources and API Gateway endpoints.

### Solution

- Enabled CORS in API Gateway
- Updated Lambda response headers
- Returned properly structured JSON output

---

# Testing

The application was tested by:

1. Accessing the CloudFront URL
2. Entering a sample user ID
3. Sending a request through API Gateway
4. Processing the request with Lambda
5. Retrieving data from DynamoDB
6. Displaying the results in the web interface

Successful retrieval of user data confirmed the integration between all three tiers.

---

# Security Considerations

- IAM-based service permissions
- CORS configuration for controlled access
- No direct database exposure
- Backend access only through API Gateway
- Serverless architecture reducing attack surface

---

# Key Learnings

Through this project I gained practical experience with:

- Serverless AWS architecture
- API Gateway integrations
- Lambda functions
- DynamoDB operations
- CloudFront content delivery
- Cross-service communication
- CORS troubleshooting
- Frontend and backend integration

---

# Business Value

This architecture provides:

- High scalability
- Reduced infrastructure management
- Cost efficiency through serverless services
- Faster global content delivery
- Improved availability and reliability

---

# Future Improvements

- User authentication with Amazon Cognito
- Infrastructure as Code using Terraform
- CI/CD deployment with GitHub Actions
- Monitoring with Amazon CloudWatch
- Custom domain with Route 53

---

# Project Status

✅ Completed

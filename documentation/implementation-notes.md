# Implementation Notes

## Project Objective

Build a serverless three-tier web application using AWS services.

---

## Presentation Tier

### Services

- Amazon S3
- Amazon CloudFront

### Purpose

- Host static frontend files
- Deliver content globally
- Improve performance using AWS edge locations

---

## Logic Tier

### Services

- Amazon API Gateway
- AWS Lambda

### Purpose

- Process API requests
- Execute application logic
- Query DynamoDB

---

## Data Tier

### Service

- Amazon DynamoDB

### Purpose

- Store application data
- Retrieve user information
- Provide low-latency database operations

---

## Testing Process

1. Uploaded frontend files to Amazon S3.
2. Created CloudFront distribution.
3. Configured API Gateway endpoint.
4. Developed Lambda function.
5. Connected DynamoDB table.
6. Tested end-to-end application workflow.

---

## Challenges Faced

### API Endpoint Issues

The frontend application failed to communicate with the API Gateway endpoint because the API URL was incorrect.

### Resolution

- Verified endpoint URL
- Updated script.js
- Reuploaded frontend files to S3

---

### CORS Errors

Browser requests were blocked because CORS was not configured properly.

### Resolution

- Enabled CORS in API Gateway
- Updated Lambda response headers
- Tested successful API communication

---

## Key Learnings

- Serverless application architecture
- API Gateway and Lambda integration
- DynamoDB operations
- CloudFront content delivery
- AWS service connectivity
- Frontend and backend integration

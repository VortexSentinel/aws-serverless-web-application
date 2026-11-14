# Architecture Configuration

## AWS Services Used

| Service | Purpose |
|----------|----------|
| Amazon S3 | Frontend Hosting |
| Amazon CloudFront | Global Content Delivery |
| Amazon API Gateway | REST API Endpoint |
| AWS Lambda | Business Logic Processing |
| Amazon DynamoDB | NoSQL Database |
| AWS IAM | Permissions and Access Control |

---

## Presentation Tier Configuration

### Amazon S3

Responsibilities:

- Host static website files
- Store frontend assets
- Provide scalable web hosting

### Amazon CloudFront

Responsibilities:

- Reduce latency
- Deliver content globally
- Improve user experience

---

## Logic Tier Configuration

### Amazon API Gateway

Responsibilities:

- Receive frontend requests
- Route traffic to Lambda
- Return API responses

### AWS Lambda

Responsibilities:

- Process incoming requests
- Query DynamoDB
- Return JSON responses

---

## Data Tier Configuration

### Amazon DynamoDB

Database Type:

```text
NoSQL
```

Partition Key:

```text
userId
```

Responsibilities:

- Store user records
- Retrieve application data
- Support scalable serverless workloads

---

## Security Configuration

### IAM Controls

- Lambda execution role
- DynamoDB access permissions
- API Gateway service permissions

### Application Security

- No direct database exposure
- API controlled through API Gateway
- IAM-based access management

---

## Network Flow

```text
User
 │
 ▼
CloudFront
 │
 ▼
Amazon S3
 │
 ▼
API Gateway
 │
 ▼
Lambda
 │
 ▼
DynamoDB
```

---

## Common Troubleshooting Areas

### API Endpoint Errors

Potential Causes:

- Incorrect API URL
- API deployment not updated

Resolution:

- Verify API Gateway endpoint
- Redeploy API changes

---

### CORS Errors

Potential Causes:

- Missing CORS configuration
- Incorrect response headers

Resolution:

- Enable CORS in API Gateway
- Return Access-Control-Allow-Origin header from Lambda

---

## Outcome

Successful integration of all AWS services resulted in a fully functional serverless three-tier web application capable of retrieving and displaying data through a cloud-native architecture.

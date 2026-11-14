# Configurations

This directory contains configuration details and architectural settings used in the AWS Serverless Three-Tier Web Application project.

## Available Documents

### Architecture Configuration

Contains:

- AWS services used
- Database configuration
- API Gateway configuration
- Lambda configuration
- Security configuration
- CloudFront configuration

## Architecture Stack

```text
Presentation Tier
├── Amazon S3
└── Amazon CloudFront

Logic Tier
├── Amazon API Gateway
└── AWS Lambda

Data Tier
└── Amazon DynamoDB
```

These configuration documents provide a high-level overview of how AWS services were integrated throughout the project.

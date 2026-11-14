# Documentation

This directory contains supporting documentation, implementation notes, and technical details for the AWS Serverless Three-Tier Web Application project.

## Available Documents

### Implementation Notes

- Architecture overview
- Service integrations
- Testing process
- Troubleshooting notes
- Key learnings

## Project Architecture

The application follows a serverless three-tier design:

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

For complete project details, refer to the main README file.

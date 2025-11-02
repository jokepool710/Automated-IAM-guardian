# Architecture Overview

The Automated IAM Guardian is designed as a serverless, event-driven AWS security system.

## Components

1. **AWS Lambda**
   - Executes the core logic for detecting and remediating IAM policy risks.
   - Triggered on a scheduled basis or via API Gateway.

2. **AWS IAM Access Analyzer**
   - Performs analysis on IAM policies to detect over-permissive access.

3. **CloudFormation Template**
   - Automates resource creation for easy deployment across environments.

4. **AWS CloudWatch (Optional)**
   - Used for monitoring Lambda execution and sending alerts.

## Workflow

1. Lambda function retrieves attached IAM policies.
2. Access Analyzer evaluates them for privilege excess.
3. Risky policies are flagged and remediated automatically.
4. Logs are generated and can be forwarded to CloudWatch or an SNS topic.

This architecture supports scalability, minimal maintenance, and consistent enforcement of least-privilege principles.

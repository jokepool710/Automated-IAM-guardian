# Automated-IAM-guardian


A serverless AWS security automation tool that detects and revokes excessive IAM privileges in real time using AWS Lambda and CloudFormation.  
This project helps enforce the principle of least privilege across AWS accounts, reducing risks caused by overly permissive IAM policies.

---

## Overview

Modern cloud environments often accumulate excessive IAM privileges over time, creating hidden security risks.  
Automated IAM Guardian continuously scans attached policies, identifies risky permissions, and remediates them automatically.

---

## Features

- **Automated Detection:** Uses AWS Access Analyzer to evaluate IAM policies for privilege excess.
- **Policy Remediation:** Automatically detaches or replaces policies granting unsafe permissions.
- **Serverless Architecture:** Deployed using AWS Lambda and CloudFormation for scalability and low maintenance.
- **Modular Design:** Easily extendable for multi-account setups or custom security workflows.

---

## Architecture

**Core Components**
- **AWS Lambda:** Executes the detection and remediation logic.
- **CloudFormation:** Deploys the Lambda function and supporting resources.
- **IAM Access Analyzer:** Performs static analysis of IAM policies.

**Workflow**
1. The Lambda function is triggered on schedule or via API.
2. It retrieves IAM users and attached policies.
3. Policies are analyzed using Access Analyzer APIs.
4. Overly permissive policies are detached or replaced.

---

## Deployment

1. Clone this repository:
   ```bash
   git clone https://github.com/jokepool710/Automated-IAM-guardian.git
   cd automated-iam-guardian

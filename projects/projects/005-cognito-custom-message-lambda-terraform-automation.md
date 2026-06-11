# Project 005: Cognito Custom Message Lambda with Terraform and S3 Template Automation

## Overview

Designed and implemented a serverless email customization solution using Amazon Cognito, AWS Lambda, Amazon S3, Terraform, and GitHub Actions.

The solution enabled customized signup verification and password reset emails while eliminating hardcoded email templates and introducing automated infrastructure management through Terraform.

## Business Problem

The organization required customized email communications for user onboarding and password recovery workflows.

A key requirement was that email templates must not be hardcoded within the application or Lambda source code.

The solution needed to provide:

* Customized signup verification emails
* Customized password reset emails
* Centralized template management
* Automated deployment
* Infrastructure as Code (IaC)
* Scalability and maintainability

## Solution Architecture

I designed and implemented a Cognito Custom Message solution that dynamically retrieves email templates from Amazon S3 during runtime.

Infrastructure provisioning and template management were automated using Terraform.

### Architecture Flow

Terraform Apply

↓

Deploy Cognito Custom Message Lambda

↓

Upload signup.hbs to Amazon S3

↓

Upload password-reset.hbs to Amazon S3

↓

Lambda retrieves template from Amazon S3

↓

Verification code is injected into template

↓

Amazon Cognito sends customized email to customer

## Infrastructure as Code

The entire solution was managed using Terraform.

Terraform was used to:

* Deploy the Cognito Custom Message Lambda
* Upload email templates to Amazon S3
* Manage Lambda configuration
* Manage infrastructure updates
* Ensure repeatable deployments across environments

This approach removed manual deployment steps and improved consistency.

## My Role and Contributions

I independently designed and implemented the solution by:

* Designing the Cognito Custom Message architecture
* Developing the AWS Lambda solution
* Designing the S3-based template management approach
* Creating Terraform resources for automated S3 template uploads
* Configuring Lambda access permissions to Amazon S3
* Integrating Amazon Cognito with the Lambda function
* Updating CI/CD workflows to install and package Lambda dependencies before deployment
* Validating Terraform deployments and infrastructure changes
* Testing signup verification and password reset workflows
* Creating and documenting the implementation through pull requests

## AWS Services and Tools Used

* Amazon Cognito
* AWS Lambda
* Amazon S3
* AWS IAM
* Terraform
* GitHub Actions
* Node.js

## Email Templates Supported

### Signup Verification Email

Provides customized account verification emails during user registration.

### Password Reset Email

Provides customized password reset emails during account recovery.

## Outcome

* Eliminated hardcoded email template management.
* Introduced centralized template storage using Amazon S3.
* Automated template deployment using Terraform.
* Improved maintainability of customer communications.
* Reduced operational effort required for template updates.
* Enabled scalable and repeatable infrastructure deployments.
* Delivered customized signup verification and password reset email experiences.

## Business Impact

The solution provided a flexible and maintainable email communication framework while meeting the organization's requirement to avoid hardcoded customer-facing templates.

The use of Terraform improved deployment consistency and ensured infrastructure changes could be managed through version-controlled code.

## Key Learnings

* Serverless architecture design
* Amazon Cognito customization
* AWS Lambda development
* Amazon S3 integrations
* Terraform Infrastructure as Code
* IAM permissions management
* CI/CD workflow enhancements
* Cloud automation best practices

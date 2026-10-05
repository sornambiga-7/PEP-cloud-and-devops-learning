# Day 7 – Terraform & AWS Infrastructure Automation

## Day Overview

Day 7 started with a revision of the concepts and hands-on tasks covered during the previous six days.

The main focus of the day was **Terraform with AWS**, where I practiced creating and managing AWS resources using Terraform configuration files in VS Code.

---

## Terraform Commands Revised

Revisited the core Terraform workflow:

```bash
terraform init
terraform validate
terraform plan
terraform apply
terraform destroy
```

### Terraform Workflow

```text
Terraform Configuration
        ↓
terraform init
        ↓
terraform validate
        ↓
terraform plan
        ↓
Review Changes
        ↓
terraform apply
        ↓
AWS Infrastructure Created
        ↓
terraform destroy
        ↓
Infrastructure Removed
```

---

# Hands-on Practice with AWS & Terraform

## 1. IAM User Management

Created an **AWS IAM user using Terraform** from VS Code.

Also practiced deleting the IAM user using Terraform.

```text
Terraform Configuration
        ↓
terraform apply
        ↓
IAM User Created
        ↓
terraform destroy
        ↓
IAM User Deleted
```

This helped me understand how Terraform can manage AWS resources instead of creating them manually through the AWS Console.

---

## 2. EC2 Instance

Practiced launching an **EC2 instance** in two different ways:

### AWS Console

Created an EC2 instance manually through the AWS Management Console.

### Terraform

Created an EC2 instance using Terraform configuration in VS Code.

```text
Terraform Code
      ↓
terraform plan
      ↓
terraform apply
      ↓
EC2 Instance Created
```

This provided a practical comparison between **manual AWS resource creation** and **Infrastructure as Code**.

I also referred to the official AWS EC2 documentation to understand the configuration and resource requirements.

---

# 3. VPC Creation using Terraform

Created and configured a basic **AWS VPC infrastructure using Terraform**.

The infrastructure included:

* VPC
* Public subnet
* Private subnet
* Internet Gateway
* Route Tables
* Route Table Associations

### Infrastructure Structure

```text
                    VPC
                     │
          ┌──────────┴──────────┐
          │                     │
     Public Subnet         Private Subnet
          │
   Internet Gateway
          │
      Route Table
```

The complete infrastructure was provisioned using Terraform from VS Code.

---

# Key Learning

Day 7 helped me understand how Terraform can be used to **automate AWS infrastructure** instead of manually creating every resource through the AWS Console.

I practiced managing:

```text
IAM
 ↓
EC2
 ↓
VPC
 ↓
Subnets
 ↓
Internet Gateway
 ↓
Route Tables
```

This gave me practical exposure to **Infrastructure as Code (IaC)** and how Terraform can be used to create, modify, and remove AWS infrastructure in a repeatable way.

## Tools Used

* Terraform
* AWS
* AWS IAM
* Amazon EC2
* Amazon VPC
* VS Code
* AWS Documentation

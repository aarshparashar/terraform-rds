# README

## Description

This Terraform configuration sets up an RDS (Relational Database Service) instance in AWS. The RDS instance is configured with MySQL 5.7, using a `db.t3.micro` instance class, with 5 GB of allocated storage. 

## Prerequisites

- AWS account with appropriate permissions.
- Terraform installed locally.

## Usage

1. Clone this repository to your local machine.
2. Modify the `provider "aws"` block in the `main.tf` file with your AWS region if needed.
3. Run `terraform init` to initialize the working directory.
4. Run `terraform apply` to create the RDS instance.
5. After verifying the plan, type `yes` to apply the changes.

## Configuration Details

- **RDS Instance:**
  - Engine: MySQL 5.7.
  - Instance Class: db.t3.micro.
  - Allocated Storage: 5 GB.
  - Database Name: demodb.
  - Username: admin.
  - Password: password.
  - Port: 3306.
  - IAM Database Authentication: Enabled.

- **Security:**
  - Security Group: Attached to a specific security group.
  - Monitoring: Enabled with a monitoring interval of 30 seconds.

- **Tags:**
  - Name: terraform-rds-aarsh.

- **Subnets:**
  - Subnet Group: Created with specified subnet IDs.

- **DB Parameter Group:**
  - Family: mysql5.7.

- **DB Option Group:**
  - Major Engine Version: 5.7.

## Notes

- Make sure to review the Terraform plan before applying changes to avoid unexpected costs or resource changes.
- This configuration is basic and may need modifications based on your specific requirements and best practices.

# S3 Bucket Versioning Enforcer with Ansible

This repository contains an Ansible playbook designed to enforce versioning on all S3 buckets within an AWS account. It interacts with AWS through the Ansible AWS collection modules, specifically targeting S3 bucket management.

## Prerequisites

- AWS account credentials with sufficient permissions to manage S3 buckets.
- Ansible installed on the local machine.
- Ansible AWS Collection installed (can be installed using `ansible-galaxy collection install amazon.aws`).
- Configured AWS credentials (`aws_access_key`, `aws_secret_access_key`) in your environment or via the AWS CLI.

## Playbook Overview

The playbook does the following tasks:

1. **Lists all S3 buckets** in the AWS account.
2. **Enforces versioning** on each S3 bucket, if it's not already enabled.

### File Structure

```bash
.
├── README.md   # This file
├── playbook.yml  # The Ansible playbook for enforcing S3 bucket versioning

# EC2 Instance Creation Using Ansible with Encrypted AWS Credentials

This project demonstrates how to create an EC2 instance on AWS using Ansible. The playbook uses encrypted credentials to ensure sensitive information like AWS access and secret keys are securely managed.

1. create random password for vault

`openssl rand -base64 2048 > vault.pass`

2. encrypting the sensitive info

`ansible-vault encrypt secret.yaml --vault-password-file vault.pass`

3. running the playbook

`ansible-playbook ec2_create.yaml --vault-password-file vault.pass`


### store the vault.pass in another location. we can also store the file which have aws passwords in another location. so when needed mention the path in the command 
  `ansible-playbook mention/the/path/ec2_create.yaml --vault-password-file mention/the/path/vault.pass`
# Terraform Installation & Basic Workflow

## Install
```bash
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt update
sudo apt install -y terraform
terraform -version
```

## Basic usage
Create `main.tf`, then run:
```bash
terraform init
terraform plan
terraform apply
```

## Tips
- Use remote backend (S3 + DynamoDB) for state locking in team environments.

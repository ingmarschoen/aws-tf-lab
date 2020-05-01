# Terraform lab for aws

create a ec2 instance with terraform.

## Requierements
```console
terraform
~/.aws/credentials
```

or SHELL ENV with export variables

```console
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
```
## Configure
- create a file e.g. ec2.tf
```console
touch ec2.tf
```

Paste the following code in ec2.tc
```console
provider "aws" {
  region     = "eu-central-1"
}

resource "aws_instance" "example" {
  ami           = "ami-076431be05aaf8080"
  instance_type = "t2.micro"
}
```

## Verify, Run and Destroy
* terraform plan
* terraform apply
* terraform destroy

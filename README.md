# Terraform lab for aws

## Minimal lab
create a ec2 instance with terraform.

### Requierements
```console
terraform
~/.aws/credentials
```

or SHELL ENV with export variables

```console
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
```
### Configure
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

### Verify, Run and Destroy
* terraform plan
* terraform apply
* terraform destroy

## Main lab 
This lab will create a VPC, network and ubuntu server with ssh login

### Requierements

```console
terraform
~/.aws/credentials
export TF_VAR_sshpubkey=`cat ~/.ssh/id_aws_lab.pub`
```
The pubkey is by design no secret but for the porpuse of demonstration it's treated as is.

### Verify
```console
terraform validate
```

### Plan
```console
terraform plan
```
### Run
```console
terraform apply
```

### Destroy
```console
terraform destroy
```



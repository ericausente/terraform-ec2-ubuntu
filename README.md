# terrform-ec2-ubuntu

## In AWS Console, Setup Programmatic Access
Add new user and key in the UserName  
 
## Attach Existing Policies and Select Admin
## Completion and Download of API Keys


As you have downloaded the API Access and Secret keys. You need to save it right so that you can use it in terraform.
Though terraform accepts the Access Key and Secret Key hardcoded with in the configuration file. It is not recommended.
Either you should save these Keys as Environment variables (or) save it as a AWS Config profile.

```
$ export AWS_ACCESS_KEY_ID=AK************IEVXQ
$ export AWS_SECRET_ACCESS_KEY=gbaIbK*********************iwN0dGfS
```
## As an AWS config Profile
In order to do this, The Simplest way is to download and setup AWS CLI:
https://www.middlewareinventory.com/blog/aws-cli-ec2/#install-cli


## Download and Install Terraform CLI

To make this precise and Short I have not added the installation instruction of Terraform. You can find the instructions here:
https://learn.hashicorp.com/terraform/getting-started/install


## Create EC2 instance with Terraform – Terraform EC2

Step1: Creating a Configuration file for Terraform AWS

    Create a Directory and Download the following file and save it as main.tf
    Execute the command terraform init to initialize
    Execute the command terraform plan to check what change would be made. ( Should always do it)
    If you are happy with the changes it is claiming to make, then execute terraform apply to commit and start the build

Step2: Initialize Terraform

```
terraform init
```

Step3: Pre-Validate the change – A pilot run
```
terraform plan
````

Step4:   Go ahead and Apply it with Terraform apply
```
terraform apply
````

Whenever we want this IP, we can come to this directory and execute  the below commands to get it: 
```
terraform output 
````



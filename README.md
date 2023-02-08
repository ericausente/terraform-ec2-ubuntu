# terrform-ec2-ubuntu

## In AWS Console...
1. Setup Programmatic Access
2. Add new user and key in the UserName  
3. Attach Existing Policies and Select Admin
4. Completion and Download of API Keys
5. Create a key-value pair, download it, and take note of the name. 
6. Take note of the VPC ID, write it somewhere. 
7. Take note of the Subnet ID, write it somewhere. 
8. Take note of the AMI IDs (you can find this during the 1st step in creating an EC2 Instance - this usually can be found on Step 1) 

Note: 
Due to some update on the version of Terraform, the "type" directive no longer needs the value of "map" to have quotation. 
Security Group and Instance Name will be automatically created based on what you have input in your terraform file. 
Only ports 22 and 80 will be opened in the Security Group Setting.
The instance name will be named SERVER01. 

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



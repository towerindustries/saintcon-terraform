
## Questions
Q1:  What is the ami argument in the aws_instance resource block, and how do you find the AMI ID for Amazon Linux 2?
Q2:  How do you specify the instance type for an EC2 instance in a Terraform configuration file?
Q3:  How do you associate a key pair with an EC2 instance using Terraform?
Q4:  How do you specify a security group for an EC2 instance in Terraform?
Q5:  How do you specify a security group for an EC2 instance in Terraform?
Q6:  How do you specify a subnet for an EC2 instance in Terraform?
Q7:  How do you specify the availability zone for an EC2 instance in Terraform?
Q8:  How do you configure an EC2 instance to run a web server on port 80 using Terraform?
Q9:  How do you attach an existing EBS volume to an EC2 instance using Terraform?
Q10:  How do you create tags for an EC2 instance using Terraform?
Q11:  What is the purpose of the output block in a Terraform configuration file, and how would you use it to output the public IP of the EC2 instance?
Q12:  How do you validate the syntax of a Terraform configuration file?
Q13:  What is the purpose of the terraform init command, and why is it necessary before deploying an EC2 instance?
Q14:  What is the purpose of the terraform plan command, and why is it useful when deploying an EC2 instance?
Q15:  What is the purpose of the terraform apply command, and what does it do in the context of deploying an EC2 instance?
Q16:  How do you destroy the resources created by a Terraform configuration file, such as an EC2 instance?




## Applied Quiz

### Question: Create a cloud-init.sh file
You are tasked with creating a file to perform initial configuration of Amazon 2023 servers.

1: Update and patch all files.
2: Install these common application.
- wget
- git
- docker
- lsof
- jq

3: Bonus Applications
- Terraform
- AWS CLI
- Azure CLI
- Python
- PIP3
- nginx
  
4: Make Configuration Changes
- Set hostname
- Configure firewalld to allow port 22, 443, and 80.

5: Bonus Applications
- Configure nginx
- Create an SSL certificate and put it on the webserver


### Question: Creating a Data Resource for Finding an AMI
You are tasked with creating a data resource in Terraform to find the latest Amazon Linux 2023 AMI. Write the Terraform code to accomplish the following:

1: The data resource should filter for AMIs that are owned by Amazon.
2: The data resource should filter for AMIs that are based on Amazon Linux 2023.
3: The data resource should select the most recent AMI that matches the filters.

### Question: Creating an EBS volume

"You are tasked with creating a new AWS EBS volume using Terraform. Write the Terraform code to accomplish the following:

1: The EBS volume should be in the us-west-2 region.
2: The volume should be of type gp2.
3: The size of the volume should be 20 GB.
4: The volume should have a tag Name with the value MyVolume."

### Question: Creating an AWS Subnet using Terraform
"You are tasked with creating a new AWS Subnet using Terraform. Write the Terraform code to accomplish the following:

1: The subnet should be in the us-west-2 region.
2: The VPC ID should be vpc-12345678.
3: The CIDR block for the subnet should be 10.0.1.0/24.
4: The availability zone for the subnet should be us-west-2a.
5: The subnet should have a tag Name with the value MySubnet."

### Question: Creating an AWS Security Group using Terraform
"You are tasked with creating a new AWS Security Group using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.
2: The VPC ID should be vpc-12345678.
3: The security group should allow inbound traffic on port 80 from any source (0.0.0.0/0).
4: The security group should allow all outbound traffic.
5: The security group should have a description My security group.
6: The security group should have a tag Name with the value my-security-group."

### Question: Creating an AWS EC2 Instance in Terraform

You are tasked with creating a new AWS EC2 instance using Terraform. Write the Terraform code to accomplish the following:

1. Create a new EC2 instance with the following specifications:
    - Instance type: t2.micro
    - AMI: Amazon Linux 2
    - Key pair: my-key-pair
    - Security group: my-security-group
    - Subnet: subnet-12345678
    - Availability zone: us-west-2a

2. Configure the EC2 instance to run a simple web server on port 80 using cloud-init.

3. Attach an existing EBS volume with the ID of the EBS Volume you created above, to the EC2 instance.

4. Create tags for the EC2 instance with the following key-value pairs:
    - Name: MyInstance
    - Environment: Production

Please provide the complete Terraform code to achieve the above requirements.


### Question: Creating an AWS EC2 Instance using a Data Resource for AMI
You are tasked with creating a new AWS EC2 instance using Terraform. The EC2 instance should use the latest Amazon Linux 2023 AMI, which you have found using a data resource. Write the Terraform code to accomplish the following:

1: The EC2 instance should be in the us-west-2 region.
2: The instance type should be t2.micro.
3: The instance should use the AMI ID obtained from the data resource.
4: The instance should be associated with the security group we created above.
5: The instance should be launched in the subnet we created above.
6: The instance should have a tag Name with the value MyEC2Instance.


### Question: Creating an EC2 Instance with User Data
You are tasked with creating a new AWS EC2 instance with user data using Terraform. Write the Terraform code to accomplish the following:

The EC2 instance should be in the us-west-2 region.
The EC2 instance should be of type t2.micro.
The EC2 instance should have user data that installs the Apache web server.


### Question: Creating an EC2 Instance with an Attached EBS Volume
You are tasked with creating a new AWS EC2 instance with an attached EBS volume using Terraform. Write the Terraform code to accomplish the following:

The EC2 instance should be in the us-west-2 region.
The EC2 instance should be of type t2.micro.
The EC2 instance should have an EBS volume of 20GB attached at /dev/sdh.
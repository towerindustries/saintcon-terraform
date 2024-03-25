# Security Group Questions


### Question: Creating a Basic Security Group
You are tasked with creating a new AWS Security Group using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.  
2: The VPC ID should be vpc-12345678.  
3: The security group should allow all outbound traffic.  
4: The security group should have a description My security group.  
5: The security group should have a tag Name with the value MySecurityGroup.  

### Question: Creating a Security Group with Specific Inbound Rules
You are tasked with creating a new AWS Security Group that allows inbound traffic on specific ports using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.  
2: The VPC ID should be one currently created or you will need to create one as part of this terraform build.  
3: The security group should allow inbound traffic on port 80 from any source (0.0.0.0/0).  
4: The security group should also allow inbound traffic on port 22 from a specific IP address (192.0.2.0/24).  
5: The security group should allow all outbound traffic.  

### Question: Creating a Security Group with Egress Rules
You are tasked with creating a new AWS Security Group that restricts outbound traffic using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.  
2: The VPC ID should be vpc-12345678.  
3: The security group should allow all inbound traffic.  
4: The security group should only allow outbound traffic to 192.0.2.0/24 on port 443.  


### Question: Creating a Security Group with Multiple Inbound and Outbound Rules
You are tasked with creating a new AWS Security Group that allows multiple inbound and outbound traffic rules using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.  
2: The VPC ID should be vpc-12345678.  
3: The security group should allow inbound traffic on port 80 and 443 from any source (0.0.0.0/0).  
4: The security group should allow outbound traffic to 192.0.2.0/24 on port 80 and 443.  

### Question: Creating a Security Group with Inbound Rules for a Specific Security Group
You are tasked with creating a new AWS Security Group that allows inbound traffic from another security group using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.  
2: The VPC ID should be vpc-12345678.  
3: The security group should allow all inbound traffic from the security group with the ID sg-0123456789abcdef0.  

### Question: Creating a Security Group with Inbound Rules for a Specific CIDR and Port Range
You are tasked with creating a new AWS Security Group that allows inbound traffic from a specific CIDR block for a range of ports using Terraform. Write the Terraform code to accomplish the following:

1: The security group should be in the us-west-2 region.  
2: The VPC ID should be vpc-12345678.  
3: The security group should allow inbound traffic on ports 6000-7000 from the CIDR block 192.0.2.0/24.  
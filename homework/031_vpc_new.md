

###Question: Creating an AWS VPC
"You are tasked with creating a new AWS VPC using Terraform. Write the Terraform code to accomplish the following:

The VPC should be in the us-west-2 region.
The CIDR block for the VPC should be 10.0.0.0/16.
The VPC should have a tag Name with the value MyVPC.

### Question: Creating Subnets in a VPC
You are tasked with creating two subnets in an existing AWS VPC using Terraform. Write the Terraform code to accomplish the following:

The subnets should be in the us-west-2 region.
The VPC ID should be the one we created above.
The CIDR blocks for the subnets should be 10.0.1.0/24 and 10.0.2.0/24.
The subnets should have tags Name with the values MySubnet1 and MySubnet2 respectively."

### Question: Creating a VPC with Public and Private Subnets
You are tasked with creating a new AWS VPC with one public subnet and one private subnet using Terraform. Write the Terraform code to accomplish the following:

The VPC and subnets should be in the us-west-2 region.
The CIDR block for the VPC should be 10.0.0.0/16.
The CIDR blocks for the subnets should be 10.0.1.0/24 (public) and 10.0.2.0/24 (private).
The public subnet should have an internet gateway attached.
The private subnet should have a NAT gateway attached."

### Question: Creating a VPC Peering Connection
You are tasked with creating a VPC peering connection between two existing AWS VPCs using Terraform. Write the Terraform code to accomplish the following:

The VPC IDs should be vpc-12345678 and vpc-87654321.
The peering connection should have a tag Name with the value MyPeeringConnection.
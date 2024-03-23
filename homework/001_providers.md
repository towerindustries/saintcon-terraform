# Providers Homework
Q1:  What is the purpose of the provider block in a Terraform configuration file when deploying an EC2 instance?
Q2:  How do you specify the AWS region in which you want to deploy your EC2 instance using Terraform?


### Question: Creating a Terraform Providers File
You are tasked with creating a new Terraform providers file. Write the Terraform code to accomplish the following:

1: The provider should be aws.
2: The AWS region should be us-west-2.
3: The AWS access key and secret key should be sourced from environment variables AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY respectively.

### Question: Configuring Terraform to Use a Remote State File
You are tasked with configuring Terraform to use a remote state file stored in an S3 bucket. Write the Terraform code to accomplish the following:

1: The backend should be s3.
2: The S3 bucket name should be my-terraform-state.
3: The key for the state file in the S3 bucket should be prod/terraform.tfstate.
4: The AWS region for the S3 bucket should be us-west-2.
5: Enable versioning for the state file.
6: Enable encryption for the state file.

### Question: Using Variables in the Terraform Providers File
You are tasked with modifying a Terraform providers file to use variables. Write the Terraform code to accomplish the following:

1: Define a variable for the AWS region.
2: Define a variable for the AWS access key.
3: Define a variable for the AWS secret key.
4: Modify the provider block to use these variables instead of hard-coded values.
5: Provide default values for these variables in a separate variables file.

### Question: Multiple Providers in a Terraform File
You are tasked with creating a Terraform providers file that includes multiple providers. Write the Terraform code to accomplish the following:

Define two providers: aws and google.
For the aws provider, the region should be us-west-2.
For the google provider, the project should be my-gcp-project, the region should be us-central1, and the zone should be us-central1-a.

### Question: Aliasing Providers in Terraform
"You are tasked with creating a Terraform providers file that includes aliased providers. Write the Terraform code to accomplish the following:

Define two aws providers with different aliases: east and west.
The east provider should use the us-east-1 region.
The west provider should use the us-west-2 region.

### Question: Configuring Provider Version in Terraform
You are tasked with creating a Terraform providers file that specifies the version of the provider to be used. Write the Terraform code to accomplish the following:

Define an aws provider.
The AWS region should be us-west-2.
The version of the aws provider should be ~> 3.0.

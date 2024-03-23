# Searching with Terraform Data

# Ami Lookups
Using Data Resource to find existing configuration information
## Convert the CLI Image Lookup to Terraform Data Resource
Step 1: Create the appropriate file name and type for terraform data lookups.
Step 2: Use the CLI image lookup command to find an example image to reference for a terraform data lookup.

Example Terraform Syntax to get you started:
```
data "aws_ami" "latest_amazon_linux_2023" {
  most_recent = true
  filter {
    name = "name"
    values = ["al2023-ami-minimal-2023*"]
  }
}
```

Q1:  What value on the first line can we set ourselves?
Q2:  What value on the first line is mandatory and cannot be changed?
Q3:  In line 4 what is the difference between name and "name"?
Q4:  What are some wild cards we can use to find a *value*?
Q5:  What is a good google search to use to find more info about using terraform data to find an ami?

# Network Lookups 
2:  Find a specific subnet address


# Answers and Hints
```
aws ec2 describe-images --region us-east-1 --image-ids ami-054aaceda83e053ee
```
```
{
    "Images": [
        {
            "Architecture": "x86_64",
            "CreationDate": "2023-03-08T20:04:35.000Z",
            "ImageId": "ami-054aaceda83e053ee",
            "ImageLocation": "amazon/amzn-ami-minimal-hvm-2018.03.0.20230306.1-x86_64-ebs",
            "ImageType": "machine",
            "Public": true,
            "OwnerId": "137112412989",
            "PlatformDetails": "Linux/UNIX",
            "UsageOperation": "RunInstances",
            "State": "available",
            "BlockDeviceMappings": [
                {
                    "DeviceName": "/dev/xvda",
                    "Ebs": {
                        "DeleteOnTermination": true,
                        "SnapshotId": "snap-0638670ad7a291d71",
                        "VolumeSize": 2,
                        "VolumeType": "standard",
                        "Encrypted": false
                    }
                }
            ],
            "Description": "Amazon Linux AMI 2018.03.0.20230306.1 x86_64 Minimal HVM ebs",
            "EnaSupport": true,
            "Hypervisor": "xen",
            "ImageOwnerAlias": "amazon",
            "Name": "amzn-ami-minimal-hvm-2018.03.0.20230306.1-x86_64-ebs",
            "RootDeviceName": "/dev/xvda",
            "RootDeviceType": "ebs",
            "SriovNetSupport": "simple",
            "VirtualizationType": "hvm",
            "DeprecationTime": "2024-01-01T00:00:00.000Z"
        }
    ]
}
```

## A Good Search Example
```
data "aws_ami" "latest_amazon_linux_2023" {
  most_recent = true
  filter {
    name = "name"
    values = ["al2023-ami-minimal-2023*"]
  }
  filter {
    name = "owner-id"
    values = ["137112412989"]
  }
  filter {
    name   = "architecture"
    values = ["x86_64"]
  }
  filter {
    name   = "virtualization-type"
    values = ["hvm"]
  }  
  filter {
    name = "owner-alias"
    values = ["amazon"]  
  }
  filter {
    name   = "state"
    values = ["available"]
  }
}
```
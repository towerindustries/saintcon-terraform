# AWS CLI Commands

### Question: Finding an AMI by Image ID
"You are tasked with finding the details of a specific AMI using the AWS CLI. Write the AWS CLI command to accomplish the following:

1: The AMI's image ID is ami-054aaceda83e053ee.
2: The command should be run in the us-east-1 region."


## Find a specific AMI

1: Get the details for the imageID *ami-054aaceda83e053ee*

## Filter on specific AMI details
1: Use the ```aws ec2 describe images``` command to find a redhat 9 image
2: Filter for the *us-east-1* region
3: Filter for the owner *amazon*
4: Filter for *x86_64* architecture


### Change Regions
1: Repeat an above search but change the *region* and redo the search.
2: Does the AMI change?

## Answers

```
aws ec2 describe-images \
    --region us-east-1 \
    --image-ids ami-054aaceda83e053ee
    --owners amazon
```



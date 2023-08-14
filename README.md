# AWS VPC with Subnets, NAT Gateway, and Internet Gateway CloudFormation Template

This CloudFormation template creates an AWS Virtual Private Cloud (VPC) with three public subnets and three private subnets. It also sets up an Internet Gateway for the public subnets and NAT Gateways for the private subnets.

## Prerequisites

- AWS account
- AWS CLI or AWS Management Console access

## How to Use

1. Clone or download this repository.

2. Deploy the CloudFormation stack using AWS CLI:

   ```bash
   aws cloudformation create-stack --stack-name MyVPCStack --template-body file://vpc-with-subnets.yaml --parameters ParameterKey=VpcCidrBlock,ParameterValue=10.0.0.0/16

Make sure to adjust the ParameterValue as needed.

Monitor the stack creation progress in the AWS Management Console or using the AWS CLI.

Once the stack is created, you can find the VPC ID, public subnet IDs, and private subnet IDs in the stack outputs.

Cleanup
Don't forget to delete the CloudFormation stack after testing:

aws cloudformation delete-stack --stack-name MyVPCStack


CloudFormation YAML template that creates an AWS Virtual Private Cloud (VPC) with three public subnets and three private subnets. It also configures an Internet Gateway and NAT Gateways for public and private subnets respectively. Additionally, it sets up route tables to manage traffic flow.

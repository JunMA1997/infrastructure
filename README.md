# infrastructure
## var
* AWS region
* VPC CIDR block
* Subnets CIDR block
* VPC name
## schema
* "VPC_CIDR":"String"
* "Subnet_CIDR_0":"String"
* "Subnet_CIDR_1":"String"
* "Subnet_CIDR_2":"String"
* "VPC_NAME":"String"
* "AWS_region":"String"
## demo command
aws cloudformation create-stack \
  --stack-name csye6225demo2 \
  --parameters ParameterKey=VPCNAME,ParameterValue=firsttest \
  ParameterKey=AWSregion,ParameterValue=us-east-1 \
  ParameterKey=SubnetCIDR0,ParameterValue=76.24.1.0/24 \
  ParameterKey=SubnetCIDR1,ParameterValue=76.24.3.0/24 \
  ParameterKey=SubnetCIDR2,ParameterValue=76.24.2.0/24 \
  ParameterKey=VPCCIDR,ParameterValue=76.24.0.0/16 \
  --profile dev \
  --template-body file://networking.json

aws cloudformation create-stack \
  --stack-name csye6225demo4 \
  --parameters file://vars.json \
  --profile dev \
  --template-body file://networking.json \
  --CAPABILITY_NAMED_IAM
# todo EC2 USERDATA THEN VALIDATE
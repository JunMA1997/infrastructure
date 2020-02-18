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
  --stack-name csye6225demo \
  --parameters ParameterKey=VPCCIDR,ParameterValue=76.24.0.0/22 \
  --parameters ParameterKey=SubnetCIDR0,ParameterValue=76.24.1.0/24 \
  --parameters ParameterKey=SubnetCIDR1,ParameterValue=76.24.3.0/23 \
  --parameters ParameterKey=SubnetCIDR2,ParameterValue=76.24.2.0/23 \
  --parameters ParameterKey=VPCNAME,ParameterValue=firsttest \
  --parameters ParameterKey=AWSregion,ParameterValue=76.24.0.0/22 \
  --region us-east-1 \
  --profile dev \
  --template-body file://networking.json
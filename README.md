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
  --parameters ParameterKey=VPC_CIDR,ParameterValue= \
  --parameters ParameterKey=Subnet_CIDR_0,ParameterValue= \
  --parameters ParameterKey=Subnet_CIDR_1,ParameterValue= \
  --parameters ParameterKey=Subnet_CIDR_2,ParameterValue= \
  --parameters ParameterKey=VPC_NAME,ParameterValue= \
  --parameters ParameterKey=AWS_region,ParameterValue= \
  --region us-east-1 \
  --profile dev\
  --template-body file://networking.json
# infrastructure(using yaml)
## var
* vars.json
## commondexample

* * aws cloudformation create-stack --stack-name csye6225 --profile dev --parameters file://vars.json --region us-east-1 --template-body file://application.yaml --capabilities CAPABILITY_NAMED_IAM

## for grading hours
### DB COMMAND
* show databases;
* use database;
* show tables;
* select * from attachment where 1
### AWS CLI DELETE S3 OBJECT
* aws s3 rm s3://csye6225demo4-s3bucket-1aqwkeqzzxcgm --recursive --profile prod --region us-east-2
### delete stack
* must delete instance for check rds
* * aws ec2 terminate-instances --instance-ids i-1234567890abcdef0
* * aws cloudformation delete-stack --stack-name csye6225demo4 --profile prod --region us-east-2*
### create CICDS3
* * aws cloudformation create-stack --stack-name CICDS3 --profile root --parameters file://S3vars.json --template-body file://S3.yaml   --capabilities CAPABILITY_NAMED_IAM

### validata tem
* * aws cloudformation validate-template --template-body file://application.yaml --profile prod
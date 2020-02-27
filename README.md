# infrastructure
## var
* vars.json
## commondexample

aws cloudformation create-stack \
  --stack-name csye6225demo4 \
  --profile prod \
  --parameters file://vars.json \
  --region us-east-2\
  --template-body file://networking.json \
  --capabilities CAPABILITY_NAMED_IAM

## for grading hours
### DB COMMAND
* show databases;
* use database;
* show tables;
* select * from attachment where 1
### AWS CLI DELETE S3 OBJECT
* aws s3 rm s3://csye6225demo4-s3bucket-1aqwkeqzzxcgm --recursive --profile prod --region us-east-2
### delete stack
aws cloudformation delete-stack   \
--stack-name csye6225demo4 \
--profile prod \
--region us-east-2*
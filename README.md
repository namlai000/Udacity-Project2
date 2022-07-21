Web link url: http://serve-webse-5nr1eh2nky75-427520313.us-east-1.elb.amazonaws.com/

Commands
Create VPC: aws cloudformation create-stack --stack-name network --template-body file://network.yml --parameters file://network-param.json --region=us-east-1 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"
Create Load Balancer and Securities: aws cloudformation create-stack --stack-name server --template-body file://server.yml --parameters file://server-param.json --region=us-east-1 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"
Delete stacks:  aws cloudformation delete-stack --stack-name network --region=us-east-1
                aws cloudformation delete-stack --stack-name server --region=us-east-1

How to do:
- run Create VPC command. wait for it finnish
- run Create Load Balancer and Securities command and wait for it finnish
- check out the web url link
 
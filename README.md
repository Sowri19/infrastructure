# INFRA

-> Procedure to configure profiles
aws configure --profile=sowrisamdev
aws configure --profile=sowridemo

-> Procedure to change profile
export AWS_PROFILE=sowrisamdev
export AWS_PROFILE=sowridemo

-> List profiles Commands
aws configure list-profiles

--> Change Regions command
export AWS_REGION=us-east-1

1--> create stack command
aws cloudformation create-stack --stack-name vpc --template-body file://cloudinfra.yaml --parameters ParameterKey=availzone1,ParameterValue=0 ParameterKey=availzone2,ParameterValue=1  ParameterKey=availzone3,ParameterValue=2 --region us-east-1 --profile sowrisamdev

2--> View stack
aws cloudformation describe-stacks --profile sowrisamdev --region us-east-1

3--> Delete Stack
aws cloudformation delete-stack --stack-name vpc1 --profile sowrisamdev --region us-east-1

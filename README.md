# INFRA
NUID: 002926129
Name: Satya Sowri Sampath Korturti

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

--> create stack command (for Assignment-3)
aws cloudformation create-stack --stack-name vpc --template-body file://cloudinfra.yaml --parameters ParameterKey=availzone1,ParameterValue=0 ParameterKey=availzone2,ParameterValue=1  ParameterKey=availzone3,ParameterValue=2 --region us-east-1 --profile sowrisamdev

--> (updated) to create stack command (for Assignment-4)
aws cloudformation create-stack --stack-name demo717 --template-body file://cloudinfra.yml --region us-east-1 --profile sowridemo --parameters ParameterKey=ImageID,ParameterValue=ami-065436957b5fd21c5

--> (Updated) to create stack command (for Assignment-5)
aws cloudformation create-stack --stack-name demostack --template-body file://cloudinfra.yml --region us-east-1 --profile sowridemo --parameters ParameterKey=AppAMIImage,ParameterValue=ami-05566675efcb6e497 ParameterKey=ACCESSKEY,ParameterValue=demokey ParameterKey=ACCESSSECRET,ParameterValue=demosecretkey --capabilities CAPABILITY_NAMED_IAM

--> Delete the stack (Assignment-5)
aws cloudformation delete-stack --stack-name test --profile sowridemo 

copy the public ip and run the endpoints in the postman

--> View stack
aws cloudformation describe-stacks --profile sowrisamdev --region us-east-1


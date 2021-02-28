# 4.4

create first a keypair named 'cloudguru'
https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#KeyPairs:

Running CFN template from CLI
```shell
STACKNAME=dynamodb-deepdive
REGION=us-east-1
PROFILE=cloudguru
aws cloudformation deploy \
  --stack-name $STACKNAME \
  --template-file cf.yaml \
  --capabilities CAPABILITY_NAMED_IAM \
  --region $REGION \
  --profile $PROFILE
```
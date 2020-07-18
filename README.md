# state-manager-inspec
Chef Inspec profile scheduled execution via AWS State Manager 

This repo has cloudformation template to create the following
  1. SSM Document
  2. SSM Association
  3. An s3 bucket to store Inspec profile

Prerequisites:
  1. SSM enabled instance
  2. Chef-cdk installed
  3. aws-sdk-ssm gem installed
  
Installation:
1. Run cloudformation template.

```aws cloudformation create-stack --stack-name StateManager --template-body file://template.yaml```

2. Copy Inspec profile to s3 bucket created.
A sample inspec profile is available here https://github.com/awslabs/aws-systems-manager/tree/master/Compliance/InSpec/PortCheck. Copy its contents to s3 bucket.

The SSM association is scheduled to run every midnight. The results are ported back to Systems Manager under configuration compliance. The association runs inspec tests on all instances tagged OS:Linux according to this configuration.




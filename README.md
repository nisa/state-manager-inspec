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

# CloudGuard CSPM AWS CloudFormation Onboarding
This Terraform project is intended to be used to onboard an AWS Public Cloud Account in CloudGuard CSPM.     
You can find the CloudFormation Templates JSON files in this folder and the direct link to launch them in your system.     
The IAM Policies that the stack will create are the public Check Point Policies [dome9 / policies](https://github.com/dome9/policies/tree/master/AWS)
 
## How to start?
At first, you will need to have a CloudGuard CSPM account; if you don't have it, you can create one with these links:
1. Create an account in [Europe Region](https://secure.eu1.dome9.com/v2/register/invite)
2. Create an account in [Asia Pacific Region](https://secure.ap1.dome9.com/v2/register/invite)
3. Create an account in [United States Region](https://secure.dome9.com/v2/register/invite)

## Prerequisite
You would need to give as a parameter the External ID that you can obtain in the onboarding wizard:
![AWS External ID](/zimages/aws-external-id.jpg)

## How to launch the template
Either copy the JSON file and then uploaded it to a newly created stack or launch the CloudFormation Templates directly.     
These are the link to launch them in your AWS Account directly.     

Use these links if your __CloudGuard Tenant is instanced in Europe__:    
1. Template with Read-Only Permission: [Launch R/O Stack](https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?templateURL=https://cspm-onboarding.s3.amazonaws.com/cft-readonly-eu.json)
2. Template with Read-Write Permission: [Launch R/W Stack](https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?templateURL=https://cspm-onboarding.s3.amazonaws.com/cft-readwrite-eu.json)
     
Use these links if your __CloudGuard Tenant is instanced in the United States__:
1. Template with Read-Only Permission: [Launch R/O Stack](https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?templateURL=https://cspm-onboarding.s3.amazonaws.com/cft-readonly.json)
2. Template with Read-Write Permission: [Launch R/W Stack](https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?templateURL=https://cspm-onboarding.s3.amazonaws.com/cft-readwrite.json)

## How to conclude the onboarding
From the Stack output copy the Role ARN:
![AWS Stack Output](/zimages/aws-role-arn.jpg)

Then copy it in the onboarding page, giving a name to the account, and then conclude the onboarding:
![AWS Complete Onboarding](/zimages/aws-completed.jpg)

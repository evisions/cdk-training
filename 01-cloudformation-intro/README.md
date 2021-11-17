# CloudFormation Intro

## What is CloudFormation?

Service that enables you to specify the cloud resources you want, configure them correctly, and not worry about how to provision, migrate, or delete those resources.

### Step 1: Deploy template to AWS

CloudFormation is driven by a template.  The template defines the resources you need with their configuration, not directions on how to create those resources. Here is the full list of template resource types you can use: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html

* Navigate to AWS CloudFormation Console (https://console.aws.amazon.com/cloudformation/home)
* Click "Create stack" and then click "With new resources"
* Enter name and parameters (will need to lookup some parameters from EC2)
* Wait for stack to finish creating by following the "Events" tab
* Inspect the resources that were created

### Step 2: Update Stack

CloudFormation manages updates so you don't have to worry about "how" those updates takes place

* Edit the `InstanceType` field to be `m5.xlarge`
* Update the existing stack in the AWS console
* Inspect how the EC2 instance was seamlessly replaced

### Step 3: Delete Stack

* Delete the stack in the AWS console


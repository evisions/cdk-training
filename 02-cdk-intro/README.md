# CDK Intro

## What is CDK?

CDK (Cloud Development Kit) is a developer-friendly library toolkit that allows for cloud resource specification via code in modern languages that then get transpiled into CloudFormation templates

### Step 1: Initialize Project

* Run `npm install -g aws-cdk`
* Create a directory for your project and move your CWD to that directory
* Run `cdk init app --language typescript`
* Edit `bin/test.ts` to specify a stack name AND a specific account/region
* Run `npx cdk synth`

![CDK Lifecycle](https://docs.aws.amazon.com/cdk/latest/guide/images/Lifecycle.png)

Further Reading on CDK concepts: https://docs.aws.amazon.com/cdk/latest/guide/home.html

### Step 2: Configure EC2 Instance

Understanding the CDK Construct tree: https://docs.aws.amazon.com/cdk/latest/guide/constructs.html#constructs_tree

CDK API Reference: https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html

* Run `npm i @aws-cdk/aws-ec2`
* Use the instance example to provision a box: https://docs.aws.amazon.com/cdk/api/latest/docs/aws-ec2-readme.html#instances
* Optional: Run `assume-role <profile> npx cdk bootstrap aws://<account>/<region>` (Reference: https://docs.aws.amazon.com/cdk/latest/guide/bootstrapping.html#bootstrapping-howto) if you have never deployed CDK to your account before
* Run `assume-role <profile> npx cdk synth`

### Step 3: Deploy to AWS

* Run `assume-role <profile> npx cdk deploy`

### Step 3: Tweak and Deploy Stack

* Run `npm i @aws-cdk/aws-iam`
* Add missing `AmazonSSMManagedInstanceCore` aws managed policy to
* Run `assume-role <profile> npx cdk deploy`
* Inspect chagnes
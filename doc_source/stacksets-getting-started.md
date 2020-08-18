# Getting started with AWS CloudFormation StackSets<a name="stacksets-getting-started"></a>

Before you create your first stack set, be sure that you have completed required account setup steps in [Prerequisites for stack set operations](stacksets-prereqs.md)\.

The template in this walkthrough enables AWS Config in a target account within the US West \(Oregon\) Region \(us\-west\-2\) and US East \(N\. Virginia\) Region \(us\-east\-1\)\. The Enable AWS Config template is located in the following S3 bucket: [https://s3\.amazonaws\.com/cloudformation\-stackset\-sample\-templates\-us\-east\-1/EnableAWSConfig\.yml](https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/EnableAWSConfig.yml)\. You can also choose this sample template in the StackSets console\.

**Topics**
+ [Create a stack set](stacksets-getting-started-create.md)
+ [Update your stack set](stacksets-update.md)
+ [Add stacks to a stack set](stackinstances-create.md)
+ [Override parameters on stack instances](stackinstances-override.md)
+ [Delete stack instances from your stack set](stackinstances-delete.md)
+ [Delete a stack set](stacksets-delete.md)
+ [Manage automatic deployments for a stack set with service\-managed permissions](stacksets-orgs-manage-auto-deployment.md)
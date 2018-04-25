# Prerequisites<a name="stacksets-prereqs"></a>

To start working with AWS CloudFormation StackSets, you should understand how AWS CloudFormation works, and have some experience working with AWS CloudFormation templates and stacks\.

Before you can get started creating your first stack set, you'll need to have the following resources and permissions created in your AWS accounts\.

+ Determine which AWS account is the *administrator account*\. Stack sets are created in this account\. A target account is the account in which you create individual stacks that belong to a stack set\.

+ Follow the instructions in this section to create roles that set up the correct administrator and target account trust relationship\. Ensure that the role that you create in the target account \(step 2\) has permissions for AWS CloudFormation to work on the resources that you have defined in your template\.


+ [Account Setup](#stacksets-prereqs-accountsetup)

## Account Setup<a name="stacksets-prereqs-accountsetup"></a>

Before you can get started, your administrator account and target accounts must have service roles configured that create a trust relationship between the accounts, and grant the target accounts permission to create and manage the resources described in your template\.

**Set up required service roles**

1. In the administrator account, create an IAM role named **AWSCloudFormationStackSetAdministrationRole**\. You can do this by creating a stack from the following AWS CloudFormation template, available online at [https://s3\.amazonaws\.com/cloudformation\-stackset\-sample\-templates\-us\-east\-1/AWSCloudFormationStackSetAdministrationRole\.yml](https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/AWSCloudFormationStackSetAdministrationRole.yml)\. The role created by this template enables the following policy on your administrator account\.

   ```
   {
       "Version": "2012-10-17",
       "Statement": [
           {
               "Action": [
                   "sts:AssumeRole"
               ],
               "Resource": [
                   "arn:aws:iam::*:role/AWSCloudFormationStackSetExecutionRole"
               ],
               "Effect": "Allow"
           }
       ]
   }
   ```

   The following trust relationship is created by the preceding template\.

   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Principal": {
           "Service": "cloudformation.amazonaws.com"
         },
         "Action": "sts:AssumeRole"
       }
     ]
   }
   ```

1. In each target account, create a service role named **AWSCloudFormationStackSetExecutionRole** that trusts the administrator account\. You can do this by creating a stack from the following AWS CloudFormation template, available online at [https://s3\.amazonaws\.com/cloudformation\-stackset\-sample\-templates\-us\-east\-1/AWSCloudFormationStackSetExecutionRole\.yml](https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/AWSCloudFormationStackSetExecutionRole.yml)\. When you use this template, you are prompted to provide the name of the administrator account with which your target account must have a trust relationship\.
**Important**  
Be aware that this template grants administrator access\. After you use the template to create a target account execution role, you must scope the permissions in the policy statement to the types of resources that you are creating by using StackSets\.

**NOTE**
The role names **AWSCloudFormationStackSetAdministrationRole** and **AWSCloudFormationStackSetExecutionRole** should be exactly named as specified since StackSet will try to look for the exact role names.

   The target account service role requires permissions to perform any operations that are specified in your AWS CloudFormation template\. For example, if your template is creating an S3 bucket, then you need permissions to create new objects for S3\. Your target account always needs full AWS CloudFormation permissions, which include permissions to create, update, delete, and describe stacks\. The role created by this template enables the following policy on a target account\.

   ```
   {
       "Version": "2012-10-17",
       "Statement": [
           {
               "Effect": "Allow",
               "Action": "*",
               "Resource": "*"
           }
       ]
   }
   ```

   The following example shows a policy statement with the minimum permissions for StackSets to work\. To create stacks in target accounts that use resources from services other than AWS CloudFormation, you must add those service actions and resources to the **AWSCloudFormationStackSetExecutionRole** policy statement for each target account\.

   ```
   {
       "Version": "2012-10-17",
       "Statement": [
           {
               "Effect": "Allow",
               "Action": 
                  [
                    "cloudformation:*",
                    "s3:*",
                    "sns:*"
                  ],
               "Resource": "*"
           }
         ]
   }
   ```

   The following trust relationship is created by the template\. The administrator account's ID is shown as *admin\_account\_id*\.

   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Principal": {
           "AWS": "arn:aws:iam::admin_account_id:root"
         },
         "Action": "sts:AssumeRole"
       }
     ]
   }
   ```

   You can configure the trust relationship of an existing target account execution role to trust a specific role in the administrator account\. If you delete the role in the administrator account, and create a new one to replace it, you must configure your target account trust relationships with the new administrator account role, represented by *admin\_account\_id* in the preceding example\.

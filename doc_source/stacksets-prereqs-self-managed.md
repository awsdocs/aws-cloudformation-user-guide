# Grant self\-managed permissions<a name="stacksets-prereqs-self-managed"></a>

To set up the required permissions for creating a **service\-managed** stack set, see [Enable trusted access with AWS Organizations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-enable-trusted-access.html)\.

Before you create a stack set with **self\-managed** permissions, you need to establish a trust relationship between the administrator and target accounts by creating IAM roles in each account\.

1. Determine which AWS account is the *administrator account*\.

   Stack sets are created in this administrator account\. A *target account* is the account in which you create individual stacks that belong to a stack set\.

1. Determine how you want to structure permissions for the stack sets\.

   The simplest \(and most permissive\) permissions configuration is where you give *all* users and groups in the administrator account the ability to create and update *all* the stack sets managed through that account\. If you need finer\-grained control, you can set up permissions to specify:
   + Which users and groups can perform stack set operations in which target accounts\.
   + Which resources users and groups can include in their stack sets\. 
   + Which stack set operations specific users and groups can perform\. 

1. Create the necessary IAM service roles in your administrator and target accounts to define the permissions you want\.
**Important**  
The role in your administrator account should be named **AWSCloudFormationStackSetAdministrationRole**\. The role in each of your target accounts should be named **AWSCloudFormationStackSetExecutionRole**\.

## Set up basic permissions for stack set operations<a name="stacksets-prereqs-accountsetup"></a>

The simplest \(and most permissive\) permissions configuration is where you give *all* users and groups in the administrator account the ability to create and update *all* the stack sets managed through that account\. To do this, you create IAM service roles for your administrator and all target accounts\. Anyone with permissions to the administrator account then has permissions to create, update, or delete any stacks in any of the target accounts\. 

Your administrator account and target accounts must have service roles configured that create a trust relationship between the accounts, and grant the target accounts permission to create and manage the resources described in your template\.

If you structure your permissions this way, users do not pass an administrator role when creating or updating stack sets\.

![\[Set up a trust relationship between the administrator account and the target accounts. Any user in the administrator account can then create any stack set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_perms_master_target.png)

**Set up permissions for all users of the administrator account to perform stack set operations in all target accounts**

1. In the administrator account, create an IAM role named **AWSCloudFormationStackSetAdministrationRole**\. The role must have this exact name\. You can do this by creating a stack from the following AWS CloudFormation template, available online at [https://s3\.amazonaws\.com/cloudformation\-stackset\-sample\-templates\-us\-east\-1/AWSCloudFormationStackSetAdministrationRole\.yml](https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/AWSCloudFormationStackSetAdministrationRole.yml)\. The role created by this template enables the following policy on your administrator account\.

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

   Be aware that to deploy stack instances into a target account that resides in a Region that is disabled by default, you will also need to include the regional service principal for that Region\. Each Region that is disabled by default will have its own regional service principal\.

   For more information on regional endpoints, including a list of endpoints, see [Regional endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints) in the *AWS General Reference Guide*\.

   The following example includes the regional service principal \(`cloudformation.ap-east-1.amazonaws.com`\) for the Asia Pacific \(Hong Kong\) region, a region which is disabled by default\.

   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Principal": {
           "Service": [
               "cloudformation.amazonaws.com",
               "cloudformation.ap-east-1.amazonaws.com"
            ]
         },
         "Action": "sts:AssumeRole"
       }
     ]
   }
   ```

   For more information, see [Prerequisites for stack set operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html#stacksets-opt-in-regions)\.

1. In each target account, create a service role named **AWSCloudFormationStackSetExecutionRole** that trusts the administrator account\. The role must have this exact name\. You can do this by creating a stack from the following AWS CloudFormation template, available online at [https://s3\.amazonaws\.com/cloudformation\-stackset\-sample\-templates\-us\-east\-1/AWSCloudFormationStackSetExecutionRole\.yml](https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/AWSCloudFormationStackSetExecutionRole.yml)\. When you use this template, you are prompted to provide the name of the administrator account with which your target account must have a trust relationship\.
**Important**  
Be aware that this template grants administrator access\. After you use the template to create a target account execution role, you must scope the permissions in the policy statement to the types of resources that you are creating by using StackSets\.

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

## Set up advanced permissions options for stack set operations<a name="stacksets-prereqs-advanced-perms"></a>

If you require finer\-grained control over the stack sets that users and groups are creating through a single administrator account, you can use IAM roles to specify:
+ Which users and groups can perform stack set operations in which target accounts\.
+ Which resources users and groups can include in their stack sets\. 
+ Which stack set operations specific users and groups can perform\. 

### Set up permissions to control target account access<a name="stacksets-prereqs-multiadmin"></a>

Use customized administrator roles to control which users and groups can perform stack set operations in which target accounts\. You might want to control which users of the administrator account can perform stack set operations in which target accounts\. To do this, you create a trust relationship between each target account and a specific customized administration role, rather than creating the **AWSCloudFormationStackSetAdministrationRole** service role in the administrator account itself\. You then enable specific users and groups to use the customized administration role when performing stack set operations in a specific target account\.

For example, you can create Role A and Role B within your administrator account\. You can give Role A permissions to access target account 1 through account 8\. You can give Role B permissions to access target account 9 through account 16\.

![\[Set up a trust relationship between a customized administrator role and the target accounts. The user then passes that role when creating the stack set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_perms_admin_target.png)

Setting up the necessary permissions involves defining a customized administrator role, creating a service role for the target account, and granting users permission to pass the customized administrator role when performing stack set operations\. 

In general, here's how it works once you have the necessary permissions in place: When creating a stack set, the user must specify a customized administrator\. The user must have permission to pass the role to AWS CloudFormation\. In addition, the customized administrator role must have a trust relationship with the target accounts specified for the stack set\. AWS CloudFormation creates the stack set and associates the customized administrator role with it\. When updating a stack set, the user must explicitly specify a customized administrator role, even if it is the same customized administrator role used with this stack set previously\. AWS CloudFormation uses that role to update the stack, subject to the requirements above\.

**Set up permissions for which users and groups can perform stack set operations in specific target accounts**

1. For each stack set, create a customized administrator role with permissions to assume the **AWSCloudFormationStackSetExecutionRole** service role in the target accounts\. 

   Create an [IAM service role](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-service.html) with a custom name, using the following permissions policy:

   ```
   {
       "Version": "2012-10-17",
       "Statement": [
           {
               "Action": [
                   "sts:AssumeRole"
               ],
               "Resource": [
                   "arn:aws:iam::target_account_id:role/AWSCloudFormationStackSetExecutionRole"
               ],
               "Effect": "Allow"
           }
       ]
   }
   ```

   Or, if you want to specify all target accounts, use the following permissions policy:

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

   You must provide the following trust policy when you create the role to define the trust relationship:

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

   Be aware that to deploy stack instances into a target account that resides in a Region that is disabled by default, you will also need to include the regional service principal for that Region\. Each Region that is disabled by default will have its own regional service principal\.

   For more information on regional endpoints, including a list of endpoints, see [Regional endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints) in the *AWS General Reference Guide*\.

   The following example includes the regional service principal \(`cloudformation.ap-east-1.amazonaws.com`\) for the Asia Pacific \(Hong Kong\) region, a region which is disabled by default\.

   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Principal": {
           "Service": [
               "cloudformation.amazonaws.com",
               "cloudformation.ap-east-1.amazonaws.com"
            ]
         },
         "Action": "sts:AssumeRole"
       }
     ]
   }
   ```

   For more information, see [Prerequisites for stack set operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html#stacksets-opt-in-regions)\.

1. In each target account, create a service role named **AWSCloudFormationStackSetExecutionRole** that trusts the customized administration role you want to use with this account\.
**Important**  
You must scope the permissions in the policy statement to the types of resources that you are creating by using StackSets\.

   The target account service role requires permissions to perform any operations that are specified in your AWS CloudFormation template\. For example, if your template is creating an S3 bucket, then you need permissions to create new objects in S3\. Your target account always needs full AWS CloudFormation permissions, which include permissions to create, update, delete, and describe stacks\. 

   The following example shows a policy statement with the *minimum* permissions for StackSets to work\. To create stacks in target accounts that use resources from services other than AWS CloudFormation, you must add those service actions and resources to the **AWSCloudFormationStackSetExecutionRole** permissions policy statement for each target account\.

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

   You must provide the following trust policy when you create the role to define the trust relationship:

   ```
   { 
     "Version": "2012-10-17", 
     "Statement": [ 
       { 
         "Effect": "Allow", 
         "Principal": { 
         "AWS": "arn:aws:iam::admin_account_id:role/customized_admin_role" 
         }, 
         "Action": "sts:AssumeRole"
       } 
     ] 
   }
   ```

1. Allow users to pass the customized administrator role when performing stack set operations\. 

   Attach an IAM permissions policy to users or groups that allows them to pass the appropriate customized administrator role when creating or updating specific stack sets\. For more information, see [Granting a user permissions to pass a role to an AWS service](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html)\. In the example below, *customized\_admin\_role* refers to the administrator role the user needs to pass\. 

   ```
   {
       "Version": "2012-10-17",
       "Statement": [{
           "Effect": "Allow",
           "Action": [
               "iam:GetRole",
               "iam:PassRole"
           ],
           "Resource": "arn:aws:iam::*:role/customized_admin_role"
       }]
   }
   ```

### Set up permissions to control stack resource inclusion<a name="stacksets-prereqs-executionrole"></a>

Use customized execution roles to control which stack resources users and groups can include in their stack sets\. For example, you might want to set up a group that can only include Amazon S3\-related resources in the stack sets they create, while another team can only include DynamoDB resources\. To do this, you create a trust relationship between the customized administrator role for each group and a customized execution role for each set of resources\. The customized execution role defines which stack resources can be included in stack sets\. The customized administrator role resides in the administrator account, while the customized execution role resides in each target account in which you want to create stack sets using the defined resources\. You then enable specific users and groups to use the customized administration role when performing stack set operations\.

For example you can create customized administrator roles A, B, and C in the administrator account\. Users and groups with permission to use Role A can create stack sets containing the stack resources specifically listed in customized execution role X, but not those in roles Y or Z, or resource not included in any execution role\.

![\[Set up a trust relationship between a customized administrator role and a customized execution role in the target accounts. The user then passes those roles when creating the stack set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_perms_admin_execution.png)

When updating a stack set, the user must explicitly specify a customized administrator role, even if it is the same customized administrator role used with this stack set previously\. AWS CloudFormation performs the update using the customized administrator role specified, so long as the user has permissions to perform operations on that stack set\.

Similarly, the user can also specify a customized execution role\. If they specify a customized execution role, AWS CloudFormation uses that role to update the stack, subject to the requirements above\. If the user does not specify a customized execution role, AWS CloudFormation performs the update using the customized execution role previously associated with the stack set, so long as the user has permissions to perform operations on that stack set\.

**Set up permissions for which resources users and groups can include in specific stack sets**

1. In the target accounts in which you want to create your stack sets, create a customized execution role that grants permissions to the services and resources that you want users and groups to be able to include in the stack sets\.

   The following example provides the minimum permissions for stack sets, along with permission to create DynamoDB tables\. 

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
           },
     {
               "Effect": "Allow",
               "Action":
                  [
                    "dynamoDb:createTable"
     ],
               "Resource": "*"
           }
       ]
   }
   ```

   You must provide the following trust policy when you create the role to define the trust relationship:

   ```
   { 
     "Version": "2012-10-17", 
     "Statement": [ 
       { 
         "Effect": "Allow", 
         "Principal": { 
         "AWS": "arn:aws:iam::admin_account_id:role/customized_admin_role" 
         }, 
         "Action": "sts:AssumeRole"
       } 
     ] 
   }
   ```

1. Create a customized administrator role in your administrator account, as detailed in [Set up advanced permissions options for stack set operationsSet up permissions to control target account access](#stacksets-prereqs-multiadmin)\. Include a trust relationship between the customized administrator role and the customized execution roles which you want it to use\.

   The following example includes an `sts::AssumeRole` policy for both the **AWSCloudFormationStackSetExecutionRole** defined for the target account, as well as a customized execution role\.

```
{
  "Version": "2012-10-17",
   "Statement": [
    {
      "Sid": "Stmt1487980684000",
      "Effect": "Allow",
      "Action": [
        "sts:AssumeRole" 
      ],
      "Resource": [ 
        "arn:aws:iam::*:role/AWSCloudFormationStackSetExecutionRole",
        "arn:aws:iam::*:role/custom_execution_role" 
      ]
    } 
  ]
}
```

### Set up permissions for specific stack set operations<a name="stacksets-prereqs-iam-actions"></a>

In addition, you can set up permissions for which user and groups can perform specific stack set operations, such as creating, updating, or deleting stack sets or stack instances\. For more information, see [Actions, resources, and condition keys for AWS CloudFormation](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_awscloudformation.html) in the *IAM User Guide*\.
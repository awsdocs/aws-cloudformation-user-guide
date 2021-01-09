# Controlling access with AWS Identity and Access Management<a name="using-iam-template"></a>

With AWS Identity and Access Management \(IAM\), you can create IAM users to control who has access to which resources in your AWS account\. You can use IAM with AWS CloudFormation to control what users can do with AWS CloudFormation, such as whether they can view stack templates, create stacks, or delete stacks\.

In addition to AWS CloudFormation actions, you can manage what AWS services and resources are available to each user\. That way, you can control which resources users can access when they use AWS CloudFormation\. For example, you can specify which users can create Amazon EC2 instances, terminate database instances, or update VPCs\. Those same permissions are applied anytime they use AWS CloudFormation to do those actions\.

For more information about all the services that you can control access to, see [AWS services that support IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_SpecificProducts.html) in *IAM User Guide*\.

**Topics**
+ [AWS CloudFormation actions](#using-iam-template-actions)
+ [AWS CloudFormation resources](#resource-level-permissions)
+ [AWS CloudFormation conditions](#using-iam-template-conditions)
+ [Acknowledging IAM resources in AWS CloudFormation templates](#using-iam-capabilities)
+ [Manage credentials for applications running on Amazon EC2 instances](#using-iam-template-manage-creds)
+ [Grant temporary access \(federated access\)](#using-iam-template-grant-access)
+ [AWS CloudFormation service role](using-iam-servicerole.md)

## AWS CloudFormation actions<a name="using-iam-template-actions"></a>

When you create a group or an IAM user in your AWS account, you can associate an IAM policy with that group or user, which specifies the permissions that you want to grant\. For example, imagine you have a group of entry\-level developers\. You can create a `Junior application developers` group that includes all entry\-level developers\. Then, you associate a policy with that group that allows users to only view AWS CloudFormation stacks\. In this scenario, you might have a policy such as the following sample:

**Example A sample policy that grants view stack permissions**  

```
{
    "Version":"2012-10-17",
    "Statement":[{
        "Effect":"Allow",
        "Action":[
            "cloudformation:DescribeStacks",
            "cloudformation:DescribeStackEvents",
            "cloudformation:DescribeStackResource",
            "cloudformation:DescribeStackResources"
        ],
        "Resource":"*"
    }]
}
```

The policy grants permissions to all `DescribeStack` API actions listed in the `Action` element\.

**Note**  
If you don't specify a stack name or ID in your statement, you must also grant the permission to use all resources for the action using the `*` wildcard for the `Resource` element\.

In addition to AWS CloudFormation actions, IAM users who create or delete stacks require additional permissions that depends on the stack templates\. For example, if you have a template that describes an Amazon SQS Queue, the user must have the corresponding permissions for Amazon SQS actions to successfully create the stack, as shown in the following sample policy:

**Example A sample policy that grants create and view stack actions and all Amazon SQS actions**  

```
{
    "Version":"2012-10-17",
    "Statement":[{
        "Effect":"Allow",
        "Action":[
            "sqs:*",
            "cloudformation:CreateStack",
            "cloudformation:DescribeStacks",
            "cloudformation:DescribeStackEvents",
            "cloudformation:DescribeStackResources",
            "cloudformation:GetTemplate",
            "cloudformation:ValidateTemplate"  
        ],
        "Resource":"*"
    }]
}
```

For a list of all AWS CloudFormation actions that you can allow or deny, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/)\.

### AWS CloudFormation console\-specific actions<a name="w7739ab1c17c21c11c16"></a>

IAM users who use the AWS CloudFormation console require additional permissions that are not required for using the AWS Command Line Interface or AWS CloudFormation APIs\. Compared to the CLI and API, the console provides additional features that require additional permissions, such as template uploads to Amazon S3 buckets and drop\-down lists for [AWS\-specific parameter types](parameters-section-structure.md#aws-specific-parameter-types)\.

For all the following actions, grant permissions to all resources; don't limit actions to specific stacks or buckets\.

The following required action is used only by the AWS CloudFormation console and is not documented in the API reference\. The action allows users to upload templates to Amazon S3 buckets\.

```
cloudformation:CreateUploadBucket
```

When users upload templates, they require the following Amazon S3 permissions:

```
s3:PutObject
s3:ListBucket
s3:GetObject
s3:CreateBucket
```

For templates with [AWS\-specific parameter types](parameters-section-structure.md#aws-specific-parameter-types), users need permissions to make the corresponding describe API calls\. For example, if a template includes the `AWS::EC2::KeyPair::KeyName` parameter type, users need permission to call the EC2 `DescribeKeyPairs` action \(this is how the console gets values for the parameter drop\-down list\)\. The following examples are actions that users need for other parameter types:

```
ec2:DescribeSecurityGroups (for the AWS::EC2::SecurityGroup::Id parameter type)
ec2:DescribeSubnets (for the Subnet::Id parameter type)
ec2:DescribeVpcs (for the AWS::EC2::VPC::Id parameter type)
```

## AWS CloudFormation resources<a name="resource-level-permissions"></a>

AWS CloudFormation supports resource\-level permissions, so you can specify actions for a specific stack, as shown in the following policy:

**Example A sample policy that denies the delete and update stack actions for the MyProductionStack**  

```
{
    "Version":"2012-10-17",
    "Statement":[{
        "Effect":"Deny",
        "Action":[
            "cloudformation:DeleteStack",
            "cloudformation:UpdateStack"
        ],
        "Resource":"arn:aws:cloudformation:us-east-1:123456789012:stack/MyProductionStack/*"
    }]
}
```

The policy above uses a wild card at the end of the stack name so that delete stack and update stack are denied on the full stack ID \(such as `arn:aws:cloudformation:us-east-1:123456789012:stack/MyProductionStack/abc9dbf0-43c2-11e3-a6e8-50fa526be49c`\) and on the stack name \(such as `MyProductionStack`\)\.

To allow `AWS::Serverless` transforms to create a change set, the policy should include the `arn:aws:cloudformation:<region>:aws:transform/Serverless-2016-10-31` resource\-level permission, as shown in the following policy:

**Example A sample policy that allows the create change set action for the transform**  

```
 {
    "Version": "2012-10-17",
    "Statement": [{
        "Effect": "Allow",
        "Action": [
            "cloudformation:CreateChangeSet"
        ],
        "Resource": "arn:aws:cloudformation:us-west-2:aws:transform/Serverless-2016-10-31"
    }]
}
```

### Sample policy that grants service\-managed stack set permissions<a name="resource-level-permissions-service-managed-stack-set"></a>

The following is a sample IAM policy that grants service\-managed stack set permissions to a principal entity \(user, role, or group\)\. A user with this policy can only perform operations on stack sets with templates containing Amazon S3 resource types \(AWS::S3::\*\) or the `AWS::SES::ConfigurationSet` resource type\. If signed in to the organization master account with ID `123456789012`, the user can also only perform operations on stack sets that target the OU with ID *ou\-1fsfsrsdsfrewr*, and can only perform operations on the stack set with ID `stack-set-id` that targets the AWS account with ID *987654321012*\.

Stack set operations fail if the stack set template contains resource types other than those specified in the policy, or if the deployment targets are OU or account IDs other than those specified in the policy for the corresponding master accounts and stack sets\.

These policy restrictions only apply when stack set operations target the `us-east-1`, `us-west-2`, or `eu-west-2` Regions\.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "cloudformation:*"
            ],
            "Resource": [
                "arn:aws:cloudformation:*:*:stackset/*",
                "arn:aws:cloudformation:*::type/resource/AWS-S3-*",
                "arn:aws:cloudformation:us-west-2::type/resource/AWS-SES-ConfigurationSet",
                "arn:aws:cloudformation::123456789012:stackset-target/*/ou-1fsfsrsdsfrewr",
                "arn:aws:cloudformation::123456789012:stackset-target/stack-set-id/987654321012"
            ],
            "Condition": {
                "ForAllValues:StringEqualsIgnoreCase": {
                    "cloudformation:TargetRegion": [
                        "us-east-1",
                        "us-west-2",
                        "eu-west-1"
                    ]
                }
            }
        }
    ]
}
```

## AWS CloudFormation conditions<a name="using-iam-template-conditions"></a>

In an IAM policy, you can optionally specify conditions that control when a policy is in effect\. For example, you can define a policy that allows IAM users to create a stack only when they specify a certain template URL\. You can define AWS CloudFormation\-specific conditions and AWS\-wide conditions, such as `DateLessThan`, which specifies when a policy stops taking effect\. For more information and a list of AWS\-wide conditions, see Condition in [IAM policy elements reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/AccessPolicyLanguage_ElementDescriptions.html#Condition) in *IAM User Guide*\.

**Note**  
Do not use the `aws:SourceIp` AWS\-wide condition\. AWS CloudFormation provisions resources by using its own IP address, not the IP address of the originating request\. For example, when you create a stack, AWS CloudFormation makes requests from its IP address to launch an EC2 instance or to create an S3 bucket, not from the IP address from the `CreateStack` call or the `aws cloudformation create-stack` command\.

The following list describes the AWS CloudFormation\-specific conditions\. These conditions are applied only when users create or update stacks:

`cloudformation:ChangeSetName`  
An AWS CloudFormation change set name that you want to associate with a policy\. Use this condition to control which change sets IAM users can execute or delete\.

`cloudformation:ImportResourceTypes`  
The template resource types that you want to associate with a policy, such as `AWS::EC2::Instance`\. Use this condition to control which resource types IAM users can work with when they import resources into a stack\. This condition is checked against the resource types that users declare in the `ResourcesToImport` parameter, which is currently supported only for CLI and API requests\. When using this parameter, you must specify all the resource types you want users to control during import operations\. For more information about the `ResourcesToImport` parameter, see the [CreateChangeSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateChangeSet.html) action in the *AWS CloudFormation API Reference*\.   
For a list of possible `ResourcesToImport`, see [Resources that support import operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)\.  
Use the three\-part resource naming convention to specify which resource types users can work with, from all resources across an organization, down to an individual resource type\.    
`organization::*`  
Specify all resource types for a given organization\.  
`organization::service_name::*`  
Specify all resource types for the specified service within a given organization\.  
`organization::service_name::resource_type`  
Specify a specific resource type\.
For example:    
`AWS::*`  
Specify all supported AWS resource types\.  
`AWS::service_name::*`  
Specify all supported resources for a specific AWS service\.  
`AWS::service_name::resource_type`  
Specify a specific AWS resource type, such as `AWS::EC2::Instance` \(all EC2 instances\)\.

`cloudformation:ResourceTypes`  
The template resource types, such as `AWS::EC2::Instance`, that you want to associate with a policy\. Use this condition to control which resource types IAM users can work with when they create or update a stack\. This condition is checked against the resource types that users declare in the `ResourceTypes` parameter, which is currently supported only for CLI and API requests\. When using this parameter, users must specify all the resource types that are in their template\. For more information about the `ResourceTypes` parameter, see the [CreateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html) action in the *AWS CloudFormation API Reference*\.  
For a list of resource types, see [AWS resource and property types reference](aws-template-resource-type-ref.md)\.  
Use the three\-part resource naming convention to specify which resource types users can work with, from all resources across an organization, down to an individual resource type\.    
`organization::*`  
Specify all resource types for a given organization\.  
`organization::service_name::*`  
Specify all resource types for the specified service within a given organization\.  
`organization::service_name::resource_type`  
Specify a specific resource type\.
For example:    
`AWS::*`  
Specify all supported AWS resource types\.  
`AWS::service_name::*`  
Specify all supported resources for a specific AWS service\.  
`AWS::service_name::resource_type`  
Specify a specific AWS resource type, such as `AWS::EC2::Instance` \(all EC2 instances\)\.  
`Alexa::ASK::*`  
Specify all resource types in the Alexa Skill Kit\.  
`Alexa::ASK::Skill`  
Specify the individual [Skill](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ask-skill.html) resource type\.  
`Custom::*`  
Specify all custom resources\.  
For more information on custom resources, see [Custom resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-custom-resources.html)\.  
`Custom::resource_type`  
Specify a specific custom resource type\.  
For more information on custom resources, see [Custom resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-custom-resources.html)\.

`cloudformation:RoleARN`  
The Amazon Resource Name \(ARN\) of an IAM service role that you want to associate with a policy\. Use this condition to control which service role IAM users can use when they work with stacks or change sets\.

`cloudformation:StackPolicyUrl`  
An Amazon S3 stack policy URL that you want to associate with a policy\. Use this condition to control which stack policies IAM users can associate with a stack during a create or update stack action\. For more information about stack policies, see [Prevent updates to stack resources](protect-stack-resources.md)\.  
To ensure that IAM users can only create or update stacks with the stack policies that you uploaded, set the S3 bucket to `read only` for those users\.

`cloudformation:TemplateUrl`  
An Amazon S3 template URL that you want to associate with a policy\. Use this condition to control which templates IAM users can use when they create or update stacks\.  
To ensure that IAM users can only create or update stacks with the templates that you uploaded, set the S3 bucket to `read only` for those users\.

### Examples<a name="w7739ab1c17c21c15c10"></a>

The following example policy allows users to use only the `https://s3.amazonaws.com/testbucket/test.template` template URL to create or update a stack\.

**Example Template URL condition**  

```
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Effect" : "Allow",
      "Action" : [ "cloudformation:CreateStack", "cloudformation:UpdateStack" ],
      "Resource" : "*",
      "Condition" : {
        "ForAllValues:StringEquals" : {
          "cloudformation:TemplateUrl" : [ "https://s3.amazonaws.com/testbucket/test.template" ]
        }
      }
    }
  ]
}
```

The following example policy allows users to complete all AWS CloudFormation operations *except* import operations\.

**Example Import resource types condition**  

```
{ 
  "Version": "2012-10-17", 
  "Statement": [ 
    { 
      "Sid": "AllowAllStackOperations",
      "Effect": "Allow", 
      "Action": "cloudformation:*", 
      "Resource": "*" 
    }, 
    { 
      "Sid": "DenyImport", 
      "Effect": "Deny", 
      "Action": "cloudformation:*", 
      "Resource": "*",
      "Condition": { 
        "ForAnyValue:StringLike": {
          "cloudformation:ImportResourceTypes": [ 
            "*" 
          ] 
        } 
      } 
    } 
  ] 
}
```

The following example policy allows all stack operations, as well as import operations only on specified resources \(in this example, `AWS::S3::Bucket`\.

**Example Import resource types condition**  

```
{ 
  "Version": "2012-10-17", 
  "Statement": [ 
    { 
      "Sid": "AllowImport",
      "Effect": "Allow", 
      "Action": "cloudformation:*", 
      "Resource": "*" 
      "Condition": { 
        "ForAllValues:StringEqualsIgnoreCase": {
          "cloudformation:ImportResourceTypes": [ 
            "AWS::S3::Bucket" 
          ] 
        } 
      } 
    } 
  ] 
}
```

The following example policy allows users to create stacks but denies requests if the stack's template include any resource from the IAM service\. The policy also requires users to specify the `ResourceTypes` parameter, which is available only for CLI and API requests\. This policy uses explicit deny statements so that if any other policy grants additional permissions, this policy always remain in effect \(an explicit deny statement always overrides an explicit allow statement\)\.

**Example Resource type condition**  

```
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Effect" : "Allow",
      "Action" : [ "cloudformation:CreateStack" ],
      "Resource" : "*"
    },
    {
      "Effect" : "Deny",
      "Action" : [ "cloudformation:CreateStack" ],
      "Resource" : "*",
      "Condition" : {
        "ForAnyValue:StringLikeIfExists" : {
          "cloudformation:ResourceTypes" : [ "AWS::IAM::*" ]
        }
      }
    },
    {
      "Effect": "Deny",
      "Action" : [ "cloudformation:CreateStack" ],
      "Resource": "*",
      "Condition": {
        "Null": {
          "cloudformation:ResourceTypes": "true"
        }
      }
    }
  ]
}
```

The following example policy is similar to the preceding example\. The policy allows users to create a stack unless the stack's template includes any resource from the IAM service\. It also requires users to specify the `ResourceTypes` parameter, which is available only for CLI and API requests\. This policy is simpler, but it doesn't use explicit deny statements\. Other policies, granting additional permissions, could override this policy\.

**Example Resource type condition**  

```
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Effect" : "Allow",
      "Action" : [ "cloudformation:CreateStack" ],
      "Resource" : "*",
      "Condition" : {
        "ForAllValues:StringNotLikeIfExists" : {
          "cloudformation:ResourceTypes" : [ "AWS::IAM::*" ]
        },
        "Null":{
          "cloudformation:ResourceTypes": "false"
        }
      }
    }
  ]
}
```

## Acknowledging IAM resources in AWS CloudFormation templates<a name="using-iam-capabilities"></a>

Before you can create a stack, AWS CloudFormation validates your template\. During validation, AWS CloudFormation checks your template for IAM resources that it might create\. IAM resources, such as an IAM user with full access, can access and modify any resource in your AWS account\. Therefore, we recommend that you review the permissions associated with each IAM resource before proceeding so that you don't unintentionally create resources with escalated permissions\. To ensure that you've done so, you must acknowledge that the template contains those resources, giving AWS CloudFormation the specified capabilities before it creates the stack\.

You can acknowledge the capabilities of AWS CloudFormation templates by using the AWS CloudFormation console, AWS Command Line Interface \(CLI\), or API:
+ In the AWS CloudFormation console, on the **Review** page of the Create Stack or Update Stack wizards, choose **I acknowledge that this template may create IAM resources**\.
+ In the CLI, when you use the [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html) and [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html) commands, specify the `CAPABILITY_IAM` or `CAPABILITY_NAMED_IAM` value for the `--capabilities` parameter\. If your template includes IAM resources, you can specify either capability\. If your template includes custom names for IAM resources, you must specify `CAPABILITY_NAMED_IAM`\.
+ In the API, when you use the [CreateStack](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html) and [UpdateStack](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStack.html) actions, specify `Capabilities.member.1=CAPABILITY_IAM` or `Capabilities.member.1=CAPABILITY_NAMED_IAM`\. If your template includes IAM resources, you can specify either capability\. If your template includes custom names for IAM resources, you must specify `CAPABILITY_NAMED_IAM`\.

**Important**  
If your template contains custom named IAM resources, don't create multiple stacks reusing the same template\. IAM resources must be globally unique within your account\. If you use the same template to create multiple stacks in different Regions, your stacks might share the same IAM resources, instead of each having a unique one\. Shared resources among stacks can have unintended consequences from which you can't recover\. For example, if you delete or update shared IAM resources in one stack, you will unintentionally modify the resources of other stacks\.

## Manage credentials for applications running on Amazon EC2 instances<a name="using-iam-template-manage-creds"></a>

If you have an application that runs on an Amazon EC2 instance and needs to make requests to AWS resources such as Amazon S3 buckets or an DynamoDB table, the application requires AWS security credentials\. However, distributing and embedding long\-term security credentials in every instance that you launch is a challenge and a potential security risk\. Instead of using long\-term credentials, like IAM user credentials, we recommend that you create an IAM role that is associated with an Amazon EC2 instance when the instance is launched\. An application can then get temporary security credentials from the Amazon EC2 instance\. You don't have to embed long\-term credentials on the instance\. Also, to make managing credentials easier, you can specify just a single role for multiple Amazon EC2 instances; you don't have to create unique credentials for each instance\.

For a template snippet that shows how to launch an instance with a role, see [IAM role template examples](quickref-iam.md#scenarios-iamroles)\.

**Note**  
Applications on instances that use temporary security credentials can call any AWS CloudFormation actions\. However, because AWS CloudFormation interacts with many other AWS services, you must verify that all the services that you want to use support temporary security credentials\. For more information, see [AWS services that support AWS STS](https://docs.aws.amazon.com/STS/latest/UsingSTS/UsingTokens.html)\.

## Grant temporary access \(federated access\)<a name="using-iam-template-grant-access"></a>

In some cases, you might want to grant users with no AWS credentials temporary access to your AWS account\. Instead of creating and deleting long\-term credentials whenever you want to grant temporary access, use AWS Security Token Service \(AWS STS\)\. For example, you can use IAM roles\. From one IAM role, you can programmatically create and then distribute many temporary security credentials \(which include an access key, secret access key, and security token\)\. These credentials have a limited life, so they cannot be used to access your AWS account after they expire\. You can also create multiple IAM roles in order to grant individual users different levels of permissions\. IAM roles are useful for scenarios like federated identities and single sign\-on\.

A federated identity is a distinct identity that you can use across multiple systems\. For enterprise users with an established on\-premises identity system \(such as LDAP or Active Directory\), you can handle all authentication with your on\-premises identity system\. After a user has been authenticated, you provide temporary security credentials from the appropriate IAM user or role\. For example, you can create an `administrators` role and a `developers` role, where administrators have full access to the AWS account and developers have permissions to work only with AWS CloudFormation stacks\. After an administrator is authenticated, the administrator is authorized to obtain temporary security credentials from the `administrators` role\. However, for developers, they can obtain temporary security credentials from only the `developers` role\.

You can also grant federated users access to the AWS Management Console\. After users authenticate with your on\-premises identity system, you can programmatically construct a temporary URL that gives direct access to the AWS Management Console\. When users use the temporary URL, they won't need to sign in to AWS because they have already been authenticated \(single sign\-on\)\. Also, because the URL is constructed from the users' temporary security credentials, the permissions that are available with those credentials determine what permissions users have in the AWS Management Console\.

You can use several different AWS STS APIs to generate temporary security credentials\. For more information about which API to use, see [Ways to get temporary security credentials](https://docs.aws.amazon.com/STS/latest/UsingSTS/Welcome.html#AccessingSTS) in *Using Temporary Security Credentials*\.

**Important**  
You cannot work with IAM when you use temporary security credentials that were generated from the `GetFederationToken` API\. Instead, if you need to work with IAM, use temporary security credentials from a role\.

AWS CloudFormation interacts with many other AWS services\. When you use temporary security credentials with AWS CloudFormation, verify that all the services that you want to use support temporary security credentials\. For more information, see [AWS services that support AWS STS](https://docs.aws.amazon.com/STS/latest/UsingSTS/UsingTokens.html)\.

For more information, see the following related resources in *Using Temporary Security Credentials*:
+ [Scenarios for granting temporary access](https://docs.aws.amazon.com/STS/latest/UsingSTS/STSUseCases.html)
+ [Giving federated users direct access to the AWS Management Console](https://docs.aws.amazon.com/STS/latest/UsingSTS/STSMgmtConsole.html)
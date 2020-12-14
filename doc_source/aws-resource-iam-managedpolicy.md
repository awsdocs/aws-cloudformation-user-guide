# AWS::IAM::ManagedPolicy<a name="aws-resource-iam-managedpolicy"></a>

Creates a new managed policy for your AWS account\.

This operation creates a policy version with a version identifier of `v1` and sets v1 as the policy's default version\. For more information about policy versions, see [Versioning for Managed Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-versions.html) in the *IAM User Guide*\.

For more information about managed policies in general, see [Managed Policies and Inline Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-managedpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-managedpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::ManagedPolicy",
  "Properties" : {
      "[Description](#cfn-iam-managedpolicy-description)" : String,
      "[Groups](#cfn-iam-managedpolicy-groups)" : [ String, ... ],
      "[ManagedPolicyName](#cfn-iam-managedpolicy-managedpolicyname)" : String,
      "[Path](#cfn-ec2-dhcpoptions-path)" : String,
      "[PolicyDocument](#cfn-iam-managedpolicy-policydocument)" : Json,
      "[Roles](#cfn-iam-managedpolicy-roles)" : [ String, ... ],
      "[Users](#cfn-iam-managedpolicy-users)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-iam-managedpolicy-syntax.yaml"></a>

```
Type: AWS::IAM::ManagedPolicy
Properties: 
  [Description](#cfn-iam-managedpolicy-description): String
  [Groups](#cfn-iam-managedpolicy-groups): 
    - String
  [ManagedPolicyName](#cfn-iam-managedpolicy-managedpolicyname): String
  [Path](#cfn-ec2-dhcpoptions-path): String
  [PolicyDocument](#cfn-iam-managedpolicy-policydocument): Json
  [Roles](#cfn-iam-managedpolicy-roles): 
    - String
  [Users](#cfn-iam-managedpolicy-users): 
    - String
```

## Properties<a name="aws-resource-iam-managedpolicy-properties"></a>

`Description`  <a name="cfn-iam-managedpolicy-description"></a>
A friendly description of the policy\.  
Typically used to store information about the permissions defined in the policy\. For example, "Grants access to production DynamoDB tables\."  
The policy description is immutable\. After a value is assigned, it cannot be changed\.  
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Groups`  <a name="cfn-iam-managedpolicy-groups"></a>
The name \(friendly name, not ARN\) of the group to attach the policy to\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedPolicyName`  <a name="cfn-iam-managedpolicy-managedpolicyname"></a>
The friendly name of the policy\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities)\.  
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple Regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a Region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-ec2-dhcpoptions-path"></a>
The path for the policy\.  
For more information about paths, see [IAM Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `((/[A-Za-z0-9\.,\+@=_-]+)*)/`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyDocument`  <a name="cfn-iam-managedpolicy-policydocument"></a>
The JSON policy document that you want to use as the content for the new policy\.  
You must provide policies in JSON format in IAM\. However, for AWS CloudFormation templates formatted in YAML, you can provide the policy in JSON or YAML format\. AWS CloudFormation always converts a YAML policy to JSON format before submitting it to IAM\.  
The [regex pattern](http://wikipedia.org/wiki/regex) used to validate this parameter is a string of characters consisting of the following:  
+ Any printable ASCII character ranging from the space character \(`\u0020`\) through the end of the ASCII character range
+ The printable characters in the Basic Latin and Latin\-1 Supplement character set \(through `\u00FF`\)
+ The special characters tab \(`\u0009`\), line feed \(`\u000A`\), and carriage return \(`\u000D`\)
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `131072`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Roles`  <a name="cfn-iam-managedpolicy-roles"></a>
The name \(friendly name, not ARN\) of the role to attach the policy to\.  
This parameter allows \(per its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
If an external policy \(such as `AWS::IAM::Policy` or `AWS::IAM::ManagedPolicy`\) has a `Ref` to a role and if a resource \(such as `AWS::ECS::Service`\) also has a `Ref` to the same role, add a `DependsOn` attribute to the resource to make the resource depend on the external policy\. This dependency ensures that the role's policy is available throughout the resource's lifecycle\. For example, when you delete a stack with an `AWS::ECS::Service` resource, the `DependsOn` attribute ensures that AWS CloudFormation deletes the `AWS::ECS::Service` resource before deleting its role's policy\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Users`  <a name="cfn-iam-managedpolicy-users"></a>
The name \(friendly name, not ARN\) of the IAM user to attach the policy to\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-managedpolicy-return-values"></a>

### Ref<a name="aws-resource-iam-managedpolicy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN\.

In the following sample, the `Ref` function returns the ARN of the `CreateTestDBPolicy` managed policy, such as `arn:aws:iam::123456789012:policy/teststack-CreateTestDBPolicy-16M23YE3CS700`\.

 `{ "Ref": "CreateTestDBPolicy" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iam-managedpolicy--examples"></a>



### Create managed policy<a name="aws-resource-iam-managedpolicy--examples--Create_managed_policy"></a>

The following example creates a managed policy and associates it with the `TestDBGroup` group\. The managed policy grants users permission to create t2\.micro database instances\. The database must use the MySQL database engine and the instance name must include the prefix `test`\.

#### JSON<a name="aws-resource-iam-managedpolicy--examples--Create_managed_policy--json"></a>

```
{
    "CreateTestDBPolicy": {
        "Type": "AWS::IAM::ManagedPolicy",
        "Properties": {
            "Description": "Policy for creating a test database",
            "Path": "/",
            "PolicyDocument": {
                "Version": "2012-10-17",
                "Statement": [
                    {
                        "Effect": "Allow",
                        "Action": "rds:CreateDBInstance",
                        "Resource": {
                            "Fn::Join": [
                                "",
                                [
                                    "arn:aws:rds:",
                                    {
                                        "Ref": "AWS::Region"
                                    },
                                    ":",
                                    {
                                        "Ref": "AWS::AccountId"
                                    },
                                    ":db:test*"
                                ]
                            ]
                        },
                        "Condition": {
                            "StringEquals": {
                                "rds:DatabaseEngine": "mysql"
                            }
                        }
                    },
                    {
                        "Effect": "Allow",
                        "Action": "rds:CreateDBInstance",
                        "Resource": {
                            "Fn::Join": [
                                "",
                                [
                                    "arn:aws:rds:",
                                    {
                                        "Ref": "AWS::Region"
                                    },
                                    ":",
                                    {
                                        "Ref": "AWS::AccountId"
                                    },
                                    ":db:test*"
                                ]
                            ]
                        },
                        "Condition": {
                            "StringEquals": {
                                "rds:DatabaseClass": "db.t2.micro"
                            }
                        }
                    }
                ]
            },
            "Groups": [
                "TestDBGroup"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-iam-managedpolicy--examples--Create_managed_policy--yaml"></a>

```
CreateTestDBPolicy:
  Type: 'AWS::IAM::ManagedPolicy'
  Properties:
    Description: Policy for creating a test database
    Path: /
    PolicyDocument:
      Version: 2012-10-17
      Statement:
        - Effect: Allow
          Action: 'rds:CreateDBInstance'
          Resource: !Join 
            - ''
            - - 'arn:aws:rds:'
              - !Ref 'AWS::Region'
              - ':'
              - !Ref 'AWS::AccountId'
              - ':db:test*'
          Condition:
            StringEquals:
              'rds:DatabaseEngine': mysql
        - Effect: Allow
          Action: 'rds:CreateDBInstance'
          Resource: !Join 
            - ''
            - - 'arn:aws:rds:'
              - !Ref 'AWS::Region'
              - ':'
              - !Ref 'AWS::AccountId'
              - ':db:test*'
          Condition:
            StringEquals:
              'rds:DatabaseClass': db.t2.micro
    Groups:
      - TestDBGroup
```

## See also<a name="aws-resource-iam-managedpolicy--seealso"></a>
+  [CreatePolicy](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreatePolicy.html) in the *AWS Identity and Access Management API Reference* 


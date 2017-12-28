# AWS::IAM::ManagedPolicy<a name="aws-resource-iam-managedpolicy"></a>

`AWS::IAM::ManagedPolicy` creates an AWS Identity and Access Management \(IAM\) managed policy for your AWS account, which you can use to apply permissions to IAM users, groups, and roles\. For more information about managed policies, see [Managed Policies and Inline Policies](http://docs.aws.amazon.com/IAM/latest/UserGuide/policies_managed-vs-inline.html) in the *IAM User Guide* guide\.


+ [Syntax](#aws-resource-iam-managedpolicy-syntax)
+ [Properties](#w3ab2c21c10d709b9)
+ [Return Values](#w3ab2c21c10d709c11)
+ [Example](#w3ab2c21c10d709c13)

## Syntax<a name="aws-resource-iam-managedpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-managedpolicy-syntax.json"></a>

```
{
  "Type": "AWS::IAM::ManagedPolicy",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-groups)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-path)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-policydocument)" : JSON object,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-roles)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-users)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-managedpolicyname)" : String
  }
}
```

### YAML<a name="aws-resource-iam-managedpolicy-syntax.yaml"></a>

```
Type: "AWS::IAM::ManagedPolicy"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-groups):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-path): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-policydocument): JSON object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-roles):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-users):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-managedpolicy-managedpolicyname): String
```

## Properties<a name="w3ab2c21c10d709b9"></a>

`Description`  
A description of the IAM policy\. For example, describe the permissions that are defined in the policy\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Groups`  
The names of IAM groups to attach to this policy\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Path`  
The path for the IAM policy\. By default, the path is `/`\. For more information, see [IAM Identifiers](http://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`PolicyDocument`  
Policies that define the permissions for this managed policy\. For more information about policy syntax, see [IAM Policy Elements Reference](http://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html) in *IAM User Guide*\.  
*Required: *Yes  
*Type*: JSON object  
AWS Identity and Access Management \(IAM\) requires that policies be in JSON format\. However, for templates formatted in YAML, you can create an IAM policy in either JSON or YAML format\. AWS CloudFormation always converts a policy to JSON format before submitting it to IAM\.
*Update requires*: No interruption

`Roles`  
The names of IAM roles to attach to this policy\.  
If a policy has a `Ref` to a role and if a resource \(such as `AWS::ECS::Service`\) also has a `Ref` to the same role, add a `DependsOn` attribute to the resource so that the resource depends on the policy\. This dependency ensures that the role's policy is available throughout the resource's lifecycle\. For example, when you delete a stack with an `AWS::ECS::Service` resource, the `DependsOn` attribute ensures that the `AWS::ECS::Service` resource can complete its deletion before its role's policy is deleted\.
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Users`  
The names of users to attach to this policy\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`ManagedPolicyName`  
A custom, friendly name for your IAM managed policy\. For valid values, see the [PolicyName](http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreatePolicy.html) parameter of the `CreatePolicy` action in the *IAM API Reference*\.  
If you don't specify a `PolicyName`, AWS CloudFormation generates a unique physical ID and uses that ID for the policy name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required: *No  
*Type*: String  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d709c11"></a>

### Ref<a name="w3ab2c21c10d709c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN\.

In the following sample, the `Ref` function returns the ARN of the `CreateTestDBPolicy` managed policy, such as `arn:aws:iam::123456789012:policy/teststack-CreateTestDBPolicy-16M23YE3CS700`\.

```
{ "Ref": "CreateTestDBPolicy" }
```

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d709c13"></a>

The following example creates a managed policy and associates it with the `TestDBGroup` group\. The managed policy grants users permission to create t2\.micro database instances\. The database must use the MySQL database engine and the instance name must include the prefix `test`\.

### JSON<a name="aws-resource-iam-managedpolicy-example.json"></a>

```
"CreateTestDBPolicy" : {
  "Type" : "AWS::IAM::ManagedPolicy",
  "Properties" : {
    "Description" : "Policy for creating a test database",
    "Path" : "/",
    "PolicyDocument" :   {
      "Version":"2012-10-17", 
      "Statement" : [{
        "Effect" : "Allow",           
        "Action" : "rds:CreateDBInstance",
        "Resource" : {"Fn::Join" : [ "", [ "arn:aws:rds:", { "Ref" : "AWS::Region" }, ":", { "Ref" : "AWS::AccountId" }, ":db:test*" ] ]}, 
        "Condition" : {
          "StringEquals" : { "rds:DatabaseEngine" : "mysql" }
        }
      },
      {
        "Effect" : "Allow",           
        "Action" : "rds:CreateDBInstance",
        "Resource" : {"Fn::Join" : [ "", [ "arn:aws:rds:", { "Ref" : "AWS::Region" }, ":", { "Ref" : "AWS::Region" }, ":db:test*" ] ]}, 
        "Condition" : {
          "StringEquals" : { "rds:DatabaseClass" : "db.t2.micro" }
        }
      }]
    },
    "Groups" : ["TestDBGroup"]
  }
}
```

### YAML<a name="aws-resource-iam-managedpolicy-example.yaml"></a>

```
CreateTestDBPolicy: 
  Type: "AWS::IAM::ManagedPolicy"
  Properties: 
    Description: "Policy for creating a test database"
    Path: "/"
    PolicyDocument: 
      Version: "2012-10-17"
      Statement: 
        - 
          Effect: "Allow"
          Action: "rds:CreateDBInstance"
          Resource: 
            Fn::Join: 
              - ""
              - 
                - "arn:aws:rds:"
                - 
                  Ref: "AWS::Region"
                - ":"
                - 
                  Ref: "AWS::AccountId"
                - ":db:test*"
          Condition: 
            StringEquals: 
              rds:DatabaseEngine: "mysql"
        - 
          Effect: "Allow"
          Action: "rds:CreateDBInstance"
          Resource: 
            Fn::Join: 
              - ""
              - 
                - "arn:aws:rds:"
                - 
                  Ref: "AWS::Region"
                - ":"
                - 
                  Ref: "AWS::Region"
                - ":db:test*"
          Condition: 
            StringEquals: 
              rds:DatabaseClass: "db.t2.micro"
    Groups: 
      - "TestDBGroup"
```
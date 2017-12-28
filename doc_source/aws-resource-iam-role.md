# AWS::IAM::Role<a name="aws-resource-iam-role"></a>

Creates an AWS Identity and Access Management \(IAM\) role\. Use an IAM role to enable applications running on an EC2 instance to securely access your AWS resources\.

For more information about IAM roles, see [Working with Roles](http://docs.aws.amazon.com/IAM/latest/UserGuide/WorkingWithRoles.html) in the *AWS Identity and Access Management User Guide*\.


+ [Syntax](#aws-resource-iam-role-syntax)
+ [Properties](#w3ab2c21c10d718c11)
+ [Return Values](#w3ab2c21c10d718c13)
+ [Template Examples](#cfn-iam-role-templateexamples)
+ [See Also](#w3ab2c21c10d718c17)

## Syntax<a name="aws-resource-iam-role-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-role-syntax.json"></a>

```
{
  "Type": "AWS::IAM::Role",
  "Properties": {
    "AssumeRolePolicyDocument": { JSON },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-role-managepolicyarns)": [ String, ... ],
    "Path": String,
    "Policies": [ Policies, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-role-rolename)": String
  }
}
```

### YAML<a name="aws-resource-iam-role-syntax.yaml"></a>

```
Type: "AWS::IAM::Role"
Properties: 
  AssumeRolePolicyDocument:
    JSON object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-role-managepolicyarns):
    - String
  Path: String
  Policies:
    - Policies
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-role-rolename): String
```

## Properties<a name="w3ab2c21c10d718c11"></a>

`AssumeRolePolicyDocument`  
The trust policy that is associated with this role\. You can associate only one assume role policy with a role\. For an example of an assume role policy, see Template Examples\. For more information about the elements that you can use in an IAM policy, see [IAM Policy Elements Reference](http://docs.aws.amazon.com//IAM/latest/UserGuide/reference_policies_elements.html) in the *IAM User Guide*\.  
*Required: *Yes  
*Type*: A JSON policy document  
AWS Identity and Access Management \(IAM\) requires that policies be in JSON format\. However, for templates formatted in YAML, you can create an IAM policy in either JSON or YAML format\. AWS CloudFormation always converts a policy to JSON format before submitting it to IAM\.
*Update requires*: No interruption

`ManagedPolicyArns`  
One or more managed policy ARNs to attach to this role\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Path`  
The path associated with this role\. For information about IAM paths, see [Friendly Names and Paths](http://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html#Identifiers_FriendlyNames) in *IAM User Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Policies`  
The policies to associate with this role\. For sample templates, see Template Examples\.  
The name of each policy for a role, user, or group must be unique\. If you don't, updates to the IAM role will fail\. 
If an external policy \(such as `AWS::IAM::Policy` or `AWS::IAM::ManagedPolicy`\) has a `Ref` to a role and if a resource \(such as `AWS::ECS::Service`\) also has a `Ref` to the same role, add a `DependsOn` attribute to the resource to make the resource depend on the external policy\. This dependency ensures that the role's policy is available throughout the resource's lifecycle\. For example, when you delete a stack with an `AWS::ECS::Service` resource, the `DependsOn` attribute ensures that AWS CloudFormation deletes the `AWS::ECS::Service` resource before deleting its role's policy\.
*Required: *No  
*Type*: List of [IAM Policies](aws-properties-iam-policy.md)  
*Update requires*: No interruption

`RoleName`  
A name for the IAM role\. For valid values, see the `RoleName` parameter for the [http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateRole.html](http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateRole.html) action in the *IAM API Reference*\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the group name\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](using-iam-template.md#using-iam-capabilities)\.  
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: Replacement

### Notes on policies for IAM roles<a name="cfn-iam-role-policynotes"></a>

For general information about IAM policies and policy documents, see [How to Write a Policy](http://docs.aws.amazon.com/IAM/latest/UserGuide/AccessPolicyLanguage_HowToWritePolicies.html) in *IAM User Guide*\.

## Return Values<a name="w3ab2c21c10d718c13"></a>

### Ref<a name="w3ab2c21c10d718c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "RootRole" }
```

For the IAM::Role with the logical ID "RootRole", `Ref` will return the resource name\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d718c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the Amazon Resource Name \(ARN\) for the instance profile\. For example:  

```
{"Fn::GetAtt" : ["MyRole", "Arn"] }
```
This will return a value such as `“arn:aws:iam::1234567890:role/MyRole-AJJHDSKSDF”`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Template Examples<a name="cfn-iam-role-templateexamples"></a>

### IAM Role with Embedded Policy and Instance Profiles<a name="w3ab2c21c10d718c15b4"></a>

This example shows an embedded Policy in the IAM::Role\. The policy is specified inline in the IAM::Role Policies property\.

#### JSON<a name="aws-resource-iam-role-example1.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "RootRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Principal": {
                     "Service": [ "ec2.amazonaws.com" ]
                  },
                  "Action": [ "sts:AssumeRole" ]
               } ]
            },
            "Path": "/",
            "Policies": [ {
               "PolicyName": "root",
               "PolicyDocument": {
                  "Version" : "2012-10-17",
                  "Statement": [ {
                     "Effect": "Allow",
                     "Action": "*",
                     "Resource": "*"
                  } ]
               }
               } ]
            }
      },
      "RootInstanceProfile": {
         "Type": "AWS::IAM::InstanceProfile",
         "Properties": {
            "Path": "/",
            "Roles": [ {
               "Ref": "RootRole"
            } ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-iam-role-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  RootRole: 
    Type: "AWS::IAM::Role"
    Properties: 
      AssumeRolePolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Principal: 
              Service: 
                - "ec2.amazonaws.com"
            Action: 
              - "sts:AssumeRole"
      Path: "/"
      Policies: 
        - 
          PolicyName: "root"
          PolicyDocument: 
            Version: "2012-10-17"
            Statement: 
              - 
                Effect: "Allow"
                Action: "*"
                Resource: "*"
  RootInstanceProfile: 
    Type: "AWS::IAM::InstanceProfile"
    Properties: 
      Path: "/"
      Roles: 
        - 
          Ref: "RootRole"
```

### IAM Role with External Policy and Instance Profiles<a name="w3ab2c21c10d718c15b8"></a>

In this example, the Policy and InstanceProfile resources are specified externally to the IAM Role\. They refer to the role by specifying its name, "RootRole", in their respective Roles properties\.

#### JSON<a name="aws-resource-iam-role-example2.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "RootRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Principal": {
                     "Service": [ "ec2.amazonaws.com" ]
                  },
                  "Action": [ "sts:AssumeRole" ]
               } ]
            },
            "Path": "/"
         }
      },
      "RolePolicies": {
         "Type": "AWS::IAM::Policy",
         "Properties": {
            "PolicyName": "root",
            "PolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Action": "*",
                  "Resource": "*"
               } ]
            },
            "Roles": [ {
               "Ref": "RootRole"
            } ]
         }
      },
      "RootInstanceProfile": {
         "Type": "AWS::IAM::InstanceProfile",
         "Properties": {
            "Path": "/",
            "Roles": [ {
               "Ref": "RootRole"
            } ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-iam-role-example2.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  RootRole: 
    Type: "AWS::IAM::Role"
    Properties: 
      AssumeRolePolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Principal: 
              Service: 
                - "ec2.amazonaws.com"
            Action: 
              - "sts:AssumeRole"
      Path: "/"
  RolePolicies: 
    Type: "AWS::IAM::Policy"
    Properties: 
      PolicyName: "root"
      PolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Action: "*"
            Resource: "*"
      Roles: 
        - 
          Ref: "RootRole"
  RootInstanceProfile: 
    Type: "AWS::IAM::InstanceProfile"
    Properties: 
      Path: "/"
      Roles: 
        - 
          Ref: "RootRole"
```

## See Also<a name="w3ab2c21c10d718c17"></a>

+ 

+ 
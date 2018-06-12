# AWS::IAM::Policy<a name="aws-resource-iam-policy"></a>

The `AWS::IAM::Policy` resource associates an IAM policy with IAM users, roles, or groups\. For more information about IAM policies, see [Overview of IAM Policies](http://docs.aws.amazon.com/IAM/latest/UserGuide/policies_overview.html) in the *IAM User Guide* guide\.

**Topics**
+ [Syntax](#aws-resource-iam-policy-syntax)
+ [Properties](#w3ab2c21c10d763b9)
+ [Return Values](#w3ab2c21c10d763c11)
+ [Examples](#w3ab2c21c10d763c13)

## Syntax<a name="aws-resource-iam-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-policy-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::Policy",
  "Properties" : { 
    "[Groups](#cfn-iam-policy-groups)" : [ String, ... ],
    "[PolicyDocument](#cfn-iam-policy-policydocument)" : JSON object,
    "[PolicyName](#cfn-iam-policy-policyname)" : String,
    "[Roles](#cfn-iam-policy-roles)" : [ String, ... ],
    "[Users](#cfn-iam-policy-users)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-iam-policy-syntax.yaml"></a>

```
Type: "AWS::IAM::Policy"
Properties: 
  [Groups](#cfn-iam-policy-groups):
    - String
  [PolicyDocument](#cfn-iam-policy-policydocument): JSON object
  [PolicyName](#cfn-iam-policy-policyname): String
  [Roles](#cfn-iam-policy-roles):
    - String
  [Users](#cfn-iam-policy-users):
    - String
```

## Properties<a name="w3ab2c21c10d763b9"></a>

`Groups`  <a name="cfn-iam-policy-groups"></a>
The names of groups to which you want to add the policy\.  
*Required*: Conditional\. You must specify at least one of the following properties: `Groups`, `Roles`, or `Users`\.  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PolicyDocument`  <a name="cfn-iam-policy-policydocument"></a>
A policy document that contains permissions to add to the specified users or groups\.  
*Required*: Yes  
*Type*: JSON object  
AWS Identity and Access Management \(IAM\) requires that policies be in JSON format\. However, for templates formatted in YAML, you can create an IAM policy in either JSON or YAML format\. AWS CloudFormation always converts a policy to JSON format before submitting it to IAM\.
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PolicyName`  <a name="cfn-iam-policy-policyname"></a>
The name of the policy\. If you specify multiple policies for an entity, specify unique names\. For example, if you specify a list of policies for an IAM role, each policy must have a unique name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Roles`  <a name="cfn-iam-policy-roles"></a>
The names of [AWS::IAM::Role](aws-resource-iam-role.md)s to which this policy will be attached\.  
If a policy has a `Ref` to a role and if a resource \(such as `AWS::ECS::Service`\) also has a `Ref` to the same role, add a `DependsOn` attribute to the resource so that the resource depends on the policy\. This dependency ensures that the role's policy is available throughout the resource's lifecycle\. For example, when you delete a stack with an `AWS::ECS::Service` resource, the `DependsOn` attribute ensures that the `AWS::ECS::Service` resource can complete its deletion before its role's policy is deleted\.
*Required*: Conditional\. You must specify at least one of the following properties: `Groups`, `Roles`, or `Users`\.  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Users`  <a name="cfn-iam-policy-users"></a>
The names of users for whom you want to add the policy\.  
*Required*: Conditional\. You must specify at least one of the following properties: `Groups`, `Roles`, or `Users`\.  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d763c11"></a>

### Ref<a name="w3ab2c21c10d763c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d763c13"></a>

### IAM Policy with policy group<a name="w3ab2c21c10d763c13b2"></a>

#### JSON<a name="aws-resource-iam-policy-example1.json"></a>

```
{
   "Type" : "AWS::IAM::Policy",
   "Properties" : {
      "PolicyName" : "CFNUsers",
      "PolicyDocument" : {
         "Version" : "2012-10-17",
         "Statement": [ {
         "Effect"   : "Allow",
         "Action"   : [
            "cloudformation:Describe*",
            "cloudformation:List*",
            "cloudformation:Get*"
         ],
         "Resource" : "*"
         } ]
      },
      "Groups" : [ { "Ref" : "CFNUserGroup" } ]
   }
}
```

#### YAML<a name="aws-resource-iam-policy-example1.yaml"></a>

```
Type: "AWS::IAM::Policy"
Properties: 
  PolicyName: "CFNUsers"
  PolicyDocument: 
    Version: "2012-10-17"
    Statement: 
      - 
        Effect: "Allow"
        Action: 
          - "cloudformation:Describe*"
          - "cloudformation:List*"
          - "cloudformation:Get*"
        Resource: "*"
  Groups: 
    - 
      Ref: "CFNUserGroup"
```

### IAM Policy with specified role<a name="w3ab2c21c10d763c13b4"></a>

#### JSON<a name="aws-resource-iam-policy-example2.json"></a>

```
{
   "Type": "AWS::IAM::Policy",
   "Properties": {
      "PolicyName": "root",
      "PolicyDocument": {
         "Version" : "2012-10-17",
         "Statement": [
            { "Effect": "Allow", "Action": "*", "Resource": "*" }
         ]
      },
      "Roles": [ { "Ref": "RootRole" } ]
   }
}
```

#### YAML<a name="aws-resource-iam-policy-example2.yaml"></a>

```
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
```
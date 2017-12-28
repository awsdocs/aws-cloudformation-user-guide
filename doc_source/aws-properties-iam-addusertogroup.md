# AWS::IAM::UserToGroupAddition<a name="aws-properties-iam-addusertogroup"></a>

The `AWS::IAM::UserToGroupAddition` type adds AWS Identity and Access Management \(IAM\) users to a group\.

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.


+ [Syntax](#aws-resource-iam-addusertogroup-syntax)
+ [Properties](#w3ab2c21c10d735c11)
+ [Return Value](#w3ab2c21c10d735c13)
+ [Template Examples](#w3ab2c21c10d735c15)

## Syntax<a name="aws-resource-iam-addusertogroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-addusertogroup-syntax.json"></a>

```
{
   "Type": "AWS::IAM::UserToGroupAddition",
   "Properties": {
      "GroupName": String,
      "Users": [ User1, ... ]
   }
}
```

### YAML<a name="aws-resource-iam-addusertogroup-syntax.yaml"></a>

```
Type: "AWS::IAM::UserToGroupAddition"
Properties: 
  GroupName: String
  Users:
    - User1
```

## Properties<a name="w3ab2c21c10d735c11"></a>

`GroupName`  
The name of group to add users to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: No interruption

`Users`  
*Required*: Yes  
*Type*: List of users  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10d735c13"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyUserToGroupAddition" }
```

For the `AWS::IAM::UserToGroupAddition` with the logical ID "MyUserToGroupAddition", `Ref` will return the AWS resource name\.

For more information about using the `Ref` function, see Ref\.

## Template Examples<a name="w3ab2c21c10d735c15"></a>

To view `AWS::IAM::UserToGroupAddition` snippets, see \.
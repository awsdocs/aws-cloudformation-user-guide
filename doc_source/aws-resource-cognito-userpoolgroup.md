# AWS::Cognito::UserPoolGroup<a name="aws-resource-cognito-userpoolgroup"></a>

The `AWS::Cognito::UserPoolGroup` resource creates a user group in an Amazon Cognito user pool\.

**Topics**
+ [Syntax](#aws-resource-cognito-userpoolgroup-syntax)
+ [Properties](#w3ab2c21c10d287b9)
+ [Return Value](#w3ab2c21c10d287c11)

## Syntax<a name="aws-resource-cognito-userpoolgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolgroup-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolGroup",
  "Properties" : {
    "[Description](#cfn-cognito-userpoolgroup-description)" : String,
    "[GroupName](#cfn-cognito-userpoolgroup-groupname)" : String,
    "[Precedence](#cfn-cognito-userpoolgroup-precedence)" : Number,
    "[RoleArn](#cfn-cognito-userpoolgroup-rolearn)" : String,
    "[UserPoolId](#cfn-cognito-userpoolgroup-userpoolid)" : String
  }
}
```

### YAML<a name="aws-resource-cognito-userpoolgroup-syntax.yaml"></a>

```
Type: "AWS::Cognito::UserPoolGroup"
Properties:
  [Description](#cfn-cognito-userpoolgroup-description): String
  [GroupName](#cfn-cognito-userpoolgroup-groupname): String
  [Precedence](#cfn-cognito-userpoolgroup-precedence): Number
  [RoleArn](#cfn-cognito-userpoolgroup-rolearn): String
  [UserPoolId](#cfn-cognito-userpoolgroup-userpoolid): String
```

## Properties<a name="w3ab2c21c10d287b9"></a>

`Description`  <a name="cfn-cognito-userpoolgroup-description"></a>
A description of the user group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
MaxLength: 2048

`GroupName`  <a name="cfn-cognito-userpoolgroup-groupname"></a>
The name of the user group\. `GroupName` must be unique\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Precedence`  <a name="cfn-cognito-userpoolgroup-precedence"></a>
A nonnegative integer value that specifies the precedence of this group relative to the other groups that a user can belong to in the user pool\. Zero is the highest `Precedence` value\. Groups with lower `Precedence` values take precedence over groups with higher or null `Precedence` values\. If a user belongs to two or more groups, the role ARN of the group with the lowest precedence value is used in the `cognito:roles` and `cognito:preferred_role` claims in the user's tokens\.  
Two groups can have the same `Precedence` value\. If this happens, neither group takes precedence over the other\. If two groups with the same `Precedence` value have the same role ARN, that role is used in the `cognito:preferred_role` claim in tokens for users in each group\. If the two groups have different role ARNs, the `cognito:preferred_role` claim is not set in users' tokens\.  
The default `Precedence` value is null\.  
*Required*: No  
*Type*: Number  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RoleArn`  <a name="cfn-cognito-userpoolgroup-rolearn"></a>
The role ARN for the group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpoolgroup-userpoolid"></a>
The user pool ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d287c11"></a>

### Ref<a name="w3ab2c21c10d287c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the name of the user pool group\. For example, `Admins`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.
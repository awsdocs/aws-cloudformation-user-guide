# AWS::Cognito::UserPoolGroup<a name="aws-resource-cognito-userpoolgroup"></a>

Specifies a new group in the identified user pool\.

Calling this action requires developer credentials\.

## Syntax<a name="aws-resource-cognito-userpoolgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolgroup-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolGroup",
  "Properties" : {
      "[Description](#cfn-cognito-userpoolgroup-description)" : String,
      "[GroupName](#cfn-cognito-userpoolgroup-groupname)" : String,
      "[Precedence](#cfn-cognito-userpoolgroup-precedence)" : Double,
      "[RoleArn](#cfn-cognito-userpoolgroup-rolearn)" : String,
      "[UserPoolId](#cfn-cognito-userpoolgroup-userpoolid)" : String
    }
}
```

### YAML<a name="aws-resource-cognito-userpoolgroup-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolGroup
Properties: 
  [Description](#cfn-cognito-userpoolgroup-description): String
  [GroupName](#cfn-cognito-userpoolgroup-groupname): String
  [Precedence](#cfn-cognito-userpoolgroup-precedence): Double
  [RoleArn](#cfn-cognito-userpoolgroup-rolearn): String
  [UserPoolId](#cfn-cognito-userpoolgroup-userpoolid): String
```

## Properties<a name="aws-resource-cognito-userpoolgroup-properties"></a>

`Description`  <a name="cfn-cognito-userpoolgroup-description"></a>
A string containing the description of the group\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-cognito-userpoolgroup-groupname"></a>
The name of the group\. Must be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Precedence`  <a name="cfn-cognito-userpoolgroup-precedence"></a>
A nonnegative integer value that specifies the precedence of this group relative to the other groups that a user can belong to in the user pool\. Zero is the highest precedence value\. Groups with lower `Precedence` values take precedence over groups with higher or null `Precedence` values\. If a user belongs to two or more groups, it is the group with the lowest precedence value whose role ARN will be used in the `cognito:roles` and `cognito:preferred_role` claims in the user's tokens\.  
Two groups can have the same `Precedence` value\. If this happens, neither group takes precedence over the other\. If two groups with the same `Precedence` have the same role ARN, that role is used in the `cognito:preferred_role` claim in tokens for users in each group\. If the two groups have different role ARNs, the `cognito:preferred_role` claim is not set in users' tokens\.  
The default `Precedence` value is null\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-cognito-userpoolgroup-rolearn"></a>
The role ARN for the group\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpoolgroup-userpoolid"></a>
The user pool ID for the user pool\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cognito-userpoolgroup-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the user pool group\. For example: `Admins`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.
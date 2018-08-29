# AWS::Cognito::UserPoolUserToGroupAttachment<a name="aws-resource-cognito-userpoolusertogroupattachment"></a>

The `AWS::Cognito::UserPoolUserToGroupAttachment` resource attaches a user to an Amazon Cognito user pool user group\. 

**Topics**
+ [Syntax](#aws-resource-cognito-userpoolusertogroupattachment-syntax)
+ [Properties](#w3ab2c21c10d296b9)
+ [Return Value](#w3ab2c21c10d296c11)

## Syntax<a name="aws-resource-cognito-userpoolusertogroupattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolusertogroupattachment-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolUserToGroupAttachment",
  "Properties" : {
    "[GroupName](#cfn-cognito-userpoolusertogroupattachment-groupname)" : String,
    "[Username](#cfn-cognito-userpoolusertogroupattachment-username)" : String,
    "[UserPoolId](#cfn-cognito-userpoolusertogroupattachment-userpoolid)" : String
  }
}
```

### YAML<a name="aws-resource-cognito-userpoolusertogroupattachment-syntax.yaml"></a>

```
Type: "AWS::Cognito::UserPoolUserToGroupAttachment"
Properties:
  [GroupName](#cfn-cognito-userpoolusertogroupattachment-groupname): String
  [Username](#cfn-cognito-userpoolusertogroupattachment-username): String
  [UserPoolId](#cfn-cognito-userpoolusertogroupattachment-userpoolid): String
```

## Properties<a name="w3ab2c21c10d296b9"></a>

`GroupName`  <a name="cfn-cognito-userpoolusertogroupattachment-groupname"></a>
The name of the group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Username`  <a name="cfn-cognito-userpoolusertogroupattachment-username"></a>
The user's user name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`UserPoolId`  <a name="cfn-cognito-userpoolusertogroupattachment-userpoolid"></a>
The ID of the user pool\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d296c11"></a>

### Ref<a name="w3ab2c21c10d296c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns a generated ID, such as `UserToGroupAttachment-YejJvzrEXAMPLE`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.
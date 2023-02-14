# AWS::Connect::User UserIdentityInfo<a name="aws-properties-connect-user-useridentityinfo"></a>

Contains information about the identity of a user\.

## Syntax<a name="aws-properties-connect-user-useridentityinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-user-useridentityinfo-syntax.json"></a>

```
{
  "[Email](#cfn-connect-user-useridentityinfo-email)" : String,
  "[FirstName](#cfn-connect-user-useridentityinfo-firstname)" : String,
  "[LastName](#cfn-connect-user-useridentityinfo-lastname)" : String
}
```

### YAML<a name="aws-properties-connect-user-useridentityinfo-syntax.yaml"></a>

```
  [Email](#cfn-connect-user-useridentityinfo-email): String
  [FirstName](#cfn-connect-user-useridentityinfo-firstname): String
  [LastName](#cfn-connect-user-useridentityinfo-lastname): String
```

## Properties<a name="aws-properties-connect-user-useridentityinfo-properties"></a>

`Email`  <a name="cfn-connect-user-useridentityinfo-email"></a>
The email address\. If you are using SAML for identity management and include this parameter, an error is returned\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirstName`  <a name="cfn-connect-user-useridentityinfo-firstname"></a>
The first name\. This is required if you are using Amazon Connect or SAML for identity management\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastName`  <a name="cfn-connect-user-useridentityinfo-lastname"></a>
The last name\. This is required if you are using Amazon Connect or SAML for identity management\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
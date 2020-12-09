# AWS::Transfer::Server IdentityProviderDetails<a name="aws-properties-transfer-server-identityproviderdetails"></a>

Required when `IdentityProviderType` is set to `API_GATEWAY`\. Accepts an array containing all of the information required to call a customer\-supplied authentication API, including the API Gateway URL\. Not required when `IdentityProviderType` is set to `SERVICE_MANAGED`\.

## Syntax<a name="aws-properties-transfer-server-identityproviderdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-identityproviderdetails-syntax.json"></a>

```
{
  "[InvocationRole](#cfn-transfer-server-identityproviderdetails-invocationrole)" : String,
  "[Url](#cfn-transfer-server-identityproviderdetails-url)" : String
}
```

### YAML<a name="aws-properties-transfer-server-identityproviderdetails-syntax.yaml"></a>

```
  [InvocationRole](#cfn-transfer-server-identityproviderdetails-invocationrole): String
  [Url](#cfn-transfer-server-identityproviderdetails-url): String
```

## Properties<a name="aws-properties-transfer-server-identityproviderdetails-properties"></a>

`InvocationRole`  <a name="cfn-transfer-server-identityproviderdetails-invocationrole"></a>
Provides the type of `InvocationRole` used to authenticate the user account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-transfer-server-identityproviderdetails-url"></a>
Provides the location of the service endpoint used to authenticate users\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-transfer-server-identityproviderdetails--seealso"></a>

[IdentityProviderDetails](https://docs.aws.amazon.com/transfer/latest/userguide/API_IdentityProviderDetails.html) in the *AWS Transfer Family User Guide*\.
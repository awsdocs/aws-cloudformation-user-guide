# AWS::Transfer::Server IdentityProviderDetails<a name="aws-properties-transfer-server-identityproviderdetails"></a>

This parameter is required when the `IdentityProviderType` is set to `API_GATEWAY`\. Accepts an array containing all of the information required to call a customer\-supplied authentication API, including the API Gateway URL\. This property is not required when the `IdentityProviderType` is set to `SERVICE_MANAGED`\.

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
The `InvocationRole` parameter provides the type of `InvocationRole` used to authenticate the user account\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-transfer-server-identityproviderdetails-url"></a>
The `Url` parameter provides contains the location of the service endpoint used to authenticate users\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`

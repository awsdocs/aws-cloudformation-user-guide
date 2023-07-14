# AWS::VerifiedPermissions::IdentitySource IdentitySourceConfiguration<a name="aws-properties-verifiedpermissions-identitysource-identitysourceconfiguration"></a>

A structure that contains configuration information used when creating or updating a new identity source\.

**Note**  
At this time, the only valid member of this structure is a Amazon Cognito user pool configuration\.  
You must specify a `userPoolArn`, and optionally, a `ClientId`\.

## Syntax<a name="aws-properties-verifiedpermissions-identitysource-identitysourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-identitysource-identitysourceconfiguration-syntax.json"></a>

```
{
  "[CognitoUserPoolConfiguration](#cfn-verifiedpermissions-identitysource-identitysourceconfiguration-cognitouserpoolconfiguration)" : CognitoUserPoolConfiguration
}
```

### YAML<a name="aws-properties-verifiedpermissions-identitysource-identitysourceconfiguration-syntax.yaml"></a>

```
  [CognitoUserPoolConfiguration](#cfn-verifiedpermissions-identitysource-identitysourceconfiguration-cognitouserpoolconfiguration): 
    CognitoUserPoolConfiguration
```

## Properties<a name="aws-properties-verifiedpermissions-identitysource-identitysourceconfiguration-properties"></a>

`CognitoUserPoolConfiguration`  <a name="cfn-verifiedpermissions-identitysource-identitysourceconfiguration-cognitouserpoolconfiguration"></a>
A structure that contains configuration information used when creating or updating an identity source that represents a connection to an Amazon Cognito user pool used as an identity provider for Verified Permissions\.  
*Required*: Yes  
*Type*: [CognitoUserPoolConfiguration](aws-properties-verifiedpermissions-identitysource-cognitouserpoolconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::VerifiedPermissions::IdentitySource CognitoUserPoolConfiguration<a name="aws-properties-verifiedpermissions-identitysource-cognitouserpoolconfiguration"></a>

A structure that contains configuration information used when creating or updating an identity source that represents a connection to an Amazon Cognito user pool used as an identity provider for Verified Permissions\.

## Syntax<a name="aws-properties-verifiedpermissions-identitysource-cognitouserpoolconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-identitysource-cognitouserpoolconfiguration-syntax.json"></a>

```
{
  "[ClientIds](#cfn-verifiedpermissions-identitysource-cognitouserpoolconfiguration-clientids)" : [ String, ... ],
  "[UserPoolArn](#cfn-verifiedpermissions-identitysource-cognitouserpoolconfiguration-userpoolarn)" : String
}
```

### YAML<a name="aws-properties-verifiedpermissions-identitysource-cognitouserpoolconfiguration-syntax.yaml"></a>

```
  [ClientIds](#cfn-verifiedpermissions-identitysource-cognitouserpoolconfiguration-clientids): 
    - String
  [UserPoolArn](#cfn-verifiedpermissions-identitysource-cognitouserpoolconfiguration-userpoolarn): String
```

## Properties<a name="aws-properties-verifiedpermissions-identitysource-cognitouserpoolconfiguration-properties"></a>

`ClientIds`  <a name="cfn-verifiedpermissions-identitysource-cognitouserpoolconfiguration-clientids"></a>
The unique application client IDs that are associated with the specified Amazon Cognito user pool\.  
Example: `"ClientIds": ["&ExampleCogClientId;"]`  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolArn`  <a name="cfn-verifiedpermissions-identitysource-cognitouserpoolconfiguration-userpoolarn"></a>
The [Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the Amazon Cognito user pool that contains the identities to be authorized\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
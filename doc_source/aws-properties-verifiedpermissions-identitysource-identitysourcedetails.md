# AWS::VerifiedPermissions::IdentitySource IdentitySourceDetails<a name="aws-properties-verifiedpermissions-identitysource-identitysourcedetails"></a>

A structure that contains configuration of the identity source\.

## Syntax<a name="aws-properties-verifiedpermissions-identitysource-identitysourcedetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-identitysource-identitysourcedetails-syntax.json"></a>

```
{
  "[ClientIds](#cfn-verifiedpermissions-identitysource-identitysourcedetails-clientids)" : [ String, ... ],
  "[DiscoveryUrl](#cfn-verifiedpermissions-identitysource-identitysourcedetails-discoveryurl)" : String,
  "[OpenIdIssuer](#cfn-verifiedpermissions-identitysource-identitysourcedetails-openidissuer)" : String,
  "[UserPoolArn](#cfn-verifiedpermissions-identitysource-identitysourcedetails-userpoolarn)" : String
}
```

### YAML<a name="aws-properties-verifiedpermissions-identitysource-identitysourcedetails-syntax.yaml"></a>

```
  [ClientIds](#cfn-verifiedpermissions-identitysource-identitysourcedetails-clientids): 
    - String
  [DiscoveryUrl](#cfn-verifiedpermissions-identitysource-identitysourcedetails-discoveryurl): String
  [OpenIdIssuer](#cfn-verifiedpermissions-identitysource-identitysourcedetails-openidissuer): String
  [UserPoolArn](#cfn-verifiedpermissions-identitysource-identitysourcedetails-userpoolarn): String
```

## Properties<a name="aws-properties-verifiedpermissions-identitysource-identitysourcedetails-properties"></a>

`ClientIds`  <a name="cfn-verifiedpermissions-identitysource-identitysourcedetails-clientids"></a>
The application client IDs associated with the specified Amazon Cognito user pool that are enabled for this identity source\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DiscoveryUrl`  <a name="cfn-verifiedpermissions-identitysource-identitysourcedetails-discoveryurl"></a>
The well\-known URL that points to this user pool's OIDC discovery endpoint\. This is a URL string in the following format\. This URL replaces the placeholders for both the AWS Region and the user pool identifier with those appropriate for this user pool\.  
`https://cognito-idp.<region>.amazonaws.com/<user-pool-id>/.well-known/openid-configuration`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenIdIssuer`  <a name="cfn-verifiedpermissions-identitysource-identitysourcedetails-openidissuer"></a>
A string that identifies the type of OIDC service represented by this identity source\.   
At this time, the only valid value is `cognito`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolArn`  <a name="cfn-verifiedpermissions-identitysource-identitysourcedetails-userpoolarn"></a>
The [Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the Amazon Cognito user pool whose identities are accessible to this Verified Permissions policy store\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
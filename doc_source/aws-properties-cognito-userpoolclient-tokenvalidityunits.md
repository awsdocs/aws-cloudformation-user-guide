# AWS::Cognito::UserPoolClient TokenValidityUnits<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits"></a>

<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits-description"></a>The `TokenValidityUnits` property type specifies the units of time for each token types' validty for a [AWS::Cognito::UserPoolClient](aws-resource-cognito-userpoolclient.md)\.

## Syntax<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits-syntax.json"></a>

```
{
  "[AccessToken](#cfn-cognito-userpoolclient-tokenvalidityunits-accesstoken)" : String,
  "[IdToken](#cfn-cognito-userpoolclient-tokenvalidityunits-idtoken)" : String,
  "[RefreshToken](#cfn-cognito-userpoolclient-tokenvalidityunits-refreshtoken)" : String
}
```

### YAML<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits-syntax.yaml"></a>

```
  [AccessToken](#cfn-cognito-userpoolclient-tokenvalidityunits-accesstoken): String
  [IdToken](#cfn-cognito-userpoolclient-tokenvalidityunits-idtoken): String
  [RefreshToken](#cfn-cognito-userpoolclient-tokenvalidityunits-refreshtoken): String
```

## Properties<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits-properties"></a>

`AccessToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-accesstoken"></a>
The unit of time for the specified validity of the AccessToken.\.  
Allowed values: `hours` \| `days` \| `minutes` \| `seconds` 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-idtoken"></a>
The unit of time for the specified validity of the IdToken.\.  
Allowed values: `hours` \| `days` \| `minutes` \| `seconds`
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-refreshtoken"></a>
The unit of time for the specified validity of the RefreshToken.\.  
Allowed values: `hours` \| `days` \| `minutes` \| `seconds`
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

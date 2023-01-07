# AWS::Cognito::UserPoolClient TokenValidityUnits<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits"></a>

The units in which the validity times are represented in\. Default for RefreshToken is days, and default for ID and access tokens are hours\.

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
A time unit in “seconds”, “minutes”, “hours” or “days” for the value in AccessTokenValidity, defaults to hours\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-idtoken"></a>
A time unit in “seconds”, “minutes”, “hours” or “days” for the value in IdTokenValidity, defaults to hours\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-refreshtoken"></a>
A time unit in “seconds”, “minutes”, “hours” or “days” for the value in RefreshTokenValidity, defaults to days\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
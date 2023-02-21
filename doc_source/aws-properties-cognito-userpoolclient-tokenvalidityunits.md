# AWS::Cognito::UserPoolClient TokenValidityUnits<a name="aws-properties-cognito-userpoolclient-tokenvalidityunits"></a>

The units in which the validity times are represented\. The default unit for RefreshToken is days, and the default for ID and access tokens is hours\.

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
 A time unit of `seconds`, `minutes`, `hours`, or `days` for the value that you set in the `AccessTokenValidity` parameter\. The default `AccessTokenValidity` time unit is hours\.  
*Required*: No  
*Type*: String  
*Allowed values*: `days | hours | minutes | seconds`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-idtoken"></a>
A time unit of `seconds`, `minutes`, `hours`, or `days` for the value that you set in the `IdTokenValidity` parameter\. The default `IdTokenValidity` time unit is hours\.  
*Required*: No  
*Type*: String  
*Allowed values*: `days | hours | minutes | seconds`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits-refreshtoken"></a>
A time unit of `seconds`, `minutes`, `hours`, or `days` for the value that you set in the `RefreshTokenValidity` parameter\. The default `RefreshTokenValidity` time unit is days\.  
*Required*: No  
*Type*: String  
*Allowed values*: `days | hours | minutes | seconds`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
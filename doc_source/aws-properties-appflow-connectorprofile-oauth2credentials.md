# AWS::AppFlow::ConnectorProfile OAuth2Credentials<a name="aws-properties-appflow-connectorprofile-oauth2credentials"></a>

The OAuth 2\.0 credentials required for OAuth 2\.0 authentication\.

## Syntax<a name="aws-properties-appflow-connectorprofile-oauth2credentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-oauth2credentials-syntax.json"></a>

```
{
  "[AccessToken](#cfn-appflow-connectorprofile-oauth2credentials-accesstoken)" : String,
  "[ClientId](#cfn-appflow-connectorprofile-oauth2credentials-clientid)" : String,
  "[ClientSecret](#cfn-appflow-connectorprofile-oauth2credentials-clientsecret)" : String,
  "[OAuthRequest](#cfn-appflow-connectorprofile-oauth2credentials-oauthrequest)" : ConnectorOAuthRequest,
  "[RefreshToken](#cfn-appflow-connectorprofile-oauth2credentials-refreshtoken)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-oauth2credentials-syntax.yaml"></a>

```
  [AccessToken](#cfn-appflow-connectorprofile-oauth2credentials-accesstoken): String
  [ClientId](#cfn-appflow-connectorprofile-oauth2credentials-clientid): String
  [ClientSecret](#cfn-appflow-connectorprofile-oauth2credentials-clientsecret): String
  [OAuthRequest](#cfn-appflow-connectorprofile-oauth2credentials-oauthrequest): 
    ConnectorOAuthRequest
  [RefreshToken](#cfn-appflow-connectorprofile-oauth2credentials-refreshtoken): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-oauth2credentials-properties"></a>

`AccessToken`  <a name="cfn-appflow-connectorprofile-oauth2credentials-accesstoken"></a>
The access token used to access the connector on your behalf\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-appflow-connectorprofile-oauth2credentials-clientid"></a>
The identifier for the desired client\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-appflow-connectorprofile-oauth2credentials-clientsecret"></a>
The client secret used by the OAuth client to authenticate to the authorization server\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthRequest`  <a name="cfn-appflow-connectorprofile-oauth2credentials-oauthrequest"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConnectorOAuthRequest](aws-properties-appflow-connectorprofile-connectoroauthrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-appflow-connectorprofile-oauth2credentials-refreshtoken"></a>
The refresh token used to refresh an expired access token\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
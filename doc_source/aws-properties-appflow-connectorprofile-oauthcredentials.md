# AWS::AppFlow::ConnectorProfile OAuthCredentials<a name="aws-properties-appflow-connectorprofile-oauthcredentials"></a>

 The OAuth credentials required for OAuth type authentication\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-oauthcredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-oauthcredentials-syntax.json"></a>

```
{
  "[AccessToken](#cfn-appflow-connectorprofile-oauthcredentials-accesstoken)" : String,
  "[ClientId](#cfn-appflow-connectorprofile-oauthcredentials-clientid)" : String,
  "[ClientSecret](#cfn-appflow-connectorprofile-oauthcredentials-clientsecret)" : String,
  "[ConnectorOAuthRequest](#cfn-appflow-connectorprofile-oauthcredentials-connectoroauthrequest)" : ConnectorOAuthRequest,
  "[RefreshToken](#cfn-appflow-connectorprofile-oauthcredentials-refreshtoken)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-oauthcredentials-syntax.yaml"></a>

```
  [AccessToken](#cfn-appflow-connectorprofile-oauthcredentials-accesstoken): String
  [ClientId](#cfn-appflow-connectorprofile-oauthcredentials-clientid): String
  [ClientSecret](#cfn-appflow-connectorprofile-oauthcredentials-clientsecret): String
  [ConnectorOAuthRequest](#cfn-appflow-connectorprofile-oauthcredentials-connectoroauthrequest): 
    ConnectorOAuthRequest
  [RefreshToken](#cfn-appflow-connectorprofile-oauthcredentials-refreshtoken): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-oauthcredentials-properties"></a>

`AccessToken`  <a name="cfn-appflow-connectorprofile-oauthcredentials-accesstoken"></a>
 The access token used to access protected SAPOData resources\.   
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-appflow-connectorprofile-oauthcredentials-clientid"></a>
 The identifier for the desired client\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-appflow-connectorprofile-oauthcredentials-clientsecret"></a>
 The client secret used by the OAuth client to authenticate to the authorization server\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorOAuthRequest`  <a name="cfn-appflow-connectorprofile-oauthcredentials-connectoroauthrequest"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConnectorOAuthRequest](aws-properties-appflow-connectorprofile-connectoroauthrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-appflow-connectorprofile-oauthcredentials-refreshtoken"></a>
 The refresh token used to refresh expired access token\.   
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
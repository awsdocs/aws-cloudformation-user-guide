# AWS::AppFlow::ConnectorProfile SlackConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials"></a>

 The `SlackConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required when using Slack\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials-syntax.json"></a>

```
{
  "[AccessToken](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-accesstoken)" : String,
  "[ClientId](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-clientid)" : String,
  "[ClientSecret](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-clientsecret)" : String,
  "[ConnectorOAuthRequest](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-connectoroauthrequest)" : ConnectorOAuthRequest
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials-syntax.yaml"></a>

```
  [AccessToken](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-accesstoken): String
  [ClientId](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-clientid): String
  [ClientSecret](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-clientsecret): String
  [ConnectorOAuthRequest](#cfn-appflow-connectorprofile-slackconnectorprofilecredentials-connectoroauthrequest): 
    ConnectorOAuthRequest
```

## Properties<a name="aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials-properties"></a>

`AccessToken`  <a name="cfn-appflow-connectorprofile-slackconnectorprofilecredentials-accesstoken"></a>
 The credentials used to access protected Slack resources\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-appflow-connectorprofile-slackconnectorprofilecredentials-clientid"></a>
 The identifier for the client\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-appflow-connectorprofile-slackconnectorprofilecredentials-clientsecret"></a>
 The client secret used by the OAuth client to authenticate to the authorization server\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorOAuthRequest`  <a name="cfn-appflow-connectorprofile-slackconnectorprofilecredentials-connectoroauthrequest"></a>
 Used by select connectors for which the OAuth workflow is supported, such as Salesforce, Google Analytics, Marketo, Zendesk, and Slack\.   
*Required*: No  
*Type*: [ConnectorOAuthRequest](aws-properties-appflow-connectorprofile-connectoroauthrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials--seealso"></a>
+ [SlackConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SlackConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.


# AWS::AppFlow::ConnectorProfile ZendeskConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials"></a>

 The `ZendeskConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required when using Zendesk\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials-syntax.json"></a>

```
{
  "[AccessToken](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-accesstoken)" : String,
  "[ClientId](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-clientid)" : String,
  "[ClientSecret](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-clientsecret)" : String,
  "[ConnectorOAuthRequest](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-connectoroauthrequest)" : ConnectorOAuthRequest
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials-syntax.yaml"></a>

```
  [AccessToken](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-accesstoken): String
  [ClientId](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-clientid): String
  [ClientSecret](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-clientsecret): String
  [ConnectorOAuthRequest](#cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-connectoroauthrequest): 
    ConnectorOAuthRequest
```

## Properties<a name="aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials-properties"></a>

`AccessToken`  <a name="cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-accesstoken"></a>
 The credentials used to access protected Zendesk resources\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-clientid"></a>
 The identifier for the desired client\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-clientsecret"></a>
 The client secret used by the OAuth client to authenticate to the authorization server\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorOAuthRequest`  <a name="cfn-appflow-connectorprofile-zendeskconnectorprofilecredentials-connectoroauthrequest"></a>
 Used by select connectors for which the OAuth workflow is supported, such as Salesforce, Google Analytics, Marketo, Zendesk, and Slack\.   
*Required*: No  
*Type*: [ConnectorOAuthRequest](aws-properties-appflow-connectorprofile-connectoroauthrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials--seealso"></a>
+ [ZendeskConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ZendeskConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.


# AWS::AppFlow::ConnectorProfile PardotConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-pardotconnectorprofilecredentials"></a>

The connector\-specific profile credentials required when using Salesforce Pardot\.

## Syntax<a name="aws-properties-appflow-connectorprofile-pardotconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-pardotconnectorprofilecredentials-syntax.json"></a>

```
{
  "[AccessToken](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-accesstoken)" : String,
  "[ClientCredentialsArn](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-clientcredentialsarn)" : String,
  "[ConnectorOAuthRequest](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-connectoroauthrequest)" : ConnectorOAuthRequest,
  "[RefreshToken](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-refreshtoken)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-pardotconnectorprofilecredentials-syntax.yaml"></a>

```
  [AccessToken](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-accesstoken): String
  [ClientCredentialsArn](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-clientcredentialsarn): String
  [ConnectorOAuthRequest](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-connectoroauthrequest): 
    ConnectorOAuthRequest
  [RefreshToken](#cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-refreshtoken): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-pardotconnectorprofilecredentials-properties"></a>

`AccessToken`  <a name="cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-accesstoken"></a>
The credentials used to access protected Salesforce Pardot resources\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientCredentialsArn`  <a name="cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-clientcredentialsarn"></a>
The secret manager ARN, which contains the client ID and client secret of the connected app\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:aws:secretsmanager:.*:[0-9]+:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorOAuthRequest`  <a name="cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-connectoroauthrequest"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConnectorOAuthRequest](aws-properties-appflow-connectorprofile-connectoroauthrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-appflow-connectorprofile-pardotconnectorprofilecredentials-refreshtoken"></a>
The credentials used to acquire new access tokens\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
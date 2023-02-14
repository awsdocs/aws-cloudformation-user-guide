# AWS::AppFlow::ConnectorProfile SlackConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-slackconnectorprofileproperties"></a>

 The `SlackConnectorProfileProperties` property type specifies the connector\-specific profile properties required when using Slack\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-slackconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-slackconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-slackconnectorprofileproperties-instanceurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-slackconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-slackconnectorprofileproperties-instanceurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-slackconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-slackconnectorprofileproperties-instanceurl"></a>
 The location of the Slack resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-slackconnectorprofileproperties--seealso"></a>
+ [SlackConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SlackConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.


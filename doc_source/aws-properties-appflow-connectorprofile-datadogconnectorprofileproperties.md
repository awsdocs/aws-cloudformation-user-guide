# AWS::AppFlow::ConnectorProfile DatadogConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties"></a>

 The `DatadogConnectorProfileProperties` property type specifies the connector\-specific profile properties required by Datadog\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-datadogconnectorprofileproperties-instanceurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-datadogconnectorprofileproperties-instanceurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-datadogconnectorprofileproperties-instanceurl"></a>
 The location of the Datadog resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties--seealso"></a>
+ [DatadogConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DatadogConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.


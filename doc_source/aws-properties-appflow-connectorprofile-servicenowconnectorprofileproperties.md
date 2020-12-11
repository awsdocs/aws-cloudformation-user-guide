# AWS::AppFlow::ConnectorProfile ServiceNowConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties"></a>

 The `ServiceNowConnectorProfileProperties` property type specifies the connector\-specific profile properties required when using ServiceNow\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-servicenowconnectorprofileproperties-instanceurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-servicenowconnectorprofileproperties-instanceurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-servicenowconnectorprofileproperties-instanceurl"></a>
 The location of the ServiceNow resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties--seealso"></a>
+ [ServiceNowConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ServiceNowConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.


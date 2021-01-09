# AWS::AppFlow::ConnectorProfile VeevaConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties"></a>

 The `VeevaConnectorProfileProperties` property type specifies the connector\-specific profile properties required when using Veeva\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-veevaconnectorprofileproperties-instanceurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-veevaconnectorprofileproperties-instanceurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-veevaconnectorprofileproperties-instanceurl"></a>
 The location of the Veeva resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties--seealso"></a>
+ [VeevaConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_VeevaConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.


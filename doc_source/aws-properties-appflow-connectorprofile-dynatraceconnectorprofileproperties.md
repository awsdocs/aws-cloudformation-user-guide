# AWS::AppFlow::ConnectorProfile DynatraceConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties"></a>

 The `DynatraceConnectorProfileProperties` property type specifies the connector\-specific profile properties required by Dynatrace\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-dynatraceconnectorprofileproperties-instanceurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-dynatraceconnectorprofileproperties-instanceurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-dynatraceconnectorprofileproperties-instanceurl"></a>
 The location of the Dynatrace resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties--seealso"></a>
+ [DynatraceConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DynatraceConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.


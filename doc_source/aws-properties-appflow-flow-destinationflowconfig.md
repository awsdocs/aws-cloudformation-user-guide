# AWS::AppFlow::Flow DestinationFlowConfig<a name="aws-properties-appflow-flow-destinationflowconfig"></a>

 The `DestinationFlowConfig` property type specifies information about the configuration of destination connectors present in the flow\. 

## Syntax<a name="aws-properties-appflow-flow-destinationflowconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-destinationflowconfig-syntax.json"></a>

```
{
  "[ConnectorProfileName](#cfn-appflow-flow-destinationflowconfig-connectorprofilename)" : String,
  "[ConnectorType](#cfn-appflow-flow-destinationflowconfig-connectortype)" : String,
  "[DestinationConnectorProperties](#cfn-appflow-flow-destinationflowconfig-destinationconnectorproperties)" : DestinationConnectorProperties
}
```

### YAML<a name="aws-properties-appflow-flow-destinationflowconfig-syntax.yaml"></a>

```
  [ConnectorProfileName](#cfn-appflow-flow-destinationflowconfig-connectorprofilename): String
  [ConnectorType](#cfn-appflow-flow-destinationflowconfig-connectortype): String
  [DestinationConnectorProperties](#cfn-appflow-flow-destinationflowconfig-destinationconnectorproperties): 
    DestinationConnectorProperties
```

## Properties<a name="aws-properties-appflow-flow-destinationflowconfig-properties"></a>

`ConnectorProfileName`  <a name="cfn-appflow-flow-destinationflowconfig-connectorprofilename"></a>
 The name of the connector profile\. This name must be unique for each connector profile in the AWS account\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `[\w/!@#+=.-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorType`  <a name="cfn-appflow-flow-destinationflowconfig-connectortype"></a>
 The type of destination connector, such as Salesforce, Amazon S3, and so on\.  
*Allowed Values*: `EventBridge | Redshift | S3 | Salesforce | Snowflake`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationConnectorProperties`  <a name="cfn-appflow-flow-destinationflowconfig-destinationconnectorproperties"></a>
 This stores the information that is required to query a particular connector\.   
*Required*: Yes  
*Type*: [DestinationConnectorProperties](aws-properties-appflow-flow-destinationconnectorproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-destinationflowconfig--seealso"></a>
+ [DestinationConnectorProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DestinationConnectorProperties.html) in the *Amazon AppFlow API Reference*\.


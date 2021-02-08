# AWS::AppFlow::Flow DestinationConnectorProperties<a name="aws-properties-appflow-flow-destinationconnectorproperties"></a>

 This stores the information that is required to query a particular connector\. 

## Syntax<a name="aws-properties-appflow-flow-destinationconnectorproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-destinationconnectorproperties-syntax.json"></a>

```
{
  "[EventBridge](#cfn-appflow-flow-destinationconnectorproperties-eventbridge)" : EventBridgeDestinationProperties,
  "[Redshift](#cfn-appflow-flow-destinationconnectorproperties-redshift)" : RedshiftDestinationProperties,
  "[S3](#cfn-appflow-flow-destinationconnectorproperties-s3)" : S3DestinationProperties,
  "[Salesforce](#cfn-appflow-flow-destinationconnectorproperties-salesforce)" : SalesforceDestinationProperties,
  "[Snowflake](#cfn-appflow-flow-destinationconnectorproperties-snowflake)" : SnowflakeDestinationProperties,
  "[Upsolver](#cfn-appflow-flow-destinationconnectorproperties-upsolver)" : UpsolverDestinationProperties
}
```

### YAML<a name="aws-properties-appflow-flow-destinationconnectorproperties-syntax.yaml"></a>

```
  [EventBridge](#cfn-appflow-flow-destinationconnectorproperties-eventbridge): 
    EventBridgeDestinationProperties
  [Redshift](#cfn-appflow-flow-destinationconnectorproperties-redshift): 
    RedshiftDestinationProperties
  [S3](#cfn-appflow-flow-destinationconnectorproperties-s3): 
    S3DestinationProperties
  [Salesforce](#cfn-appflow-flow-destinationconnectorproperties-salesforce): 
    SalesforceDestinationProperties
  [Snowflake](#cfn-appflow-flow-destinationconnectorproperties-snowflake): 
    SnowflakeDestinationProperties
  [Upsolver](#cfn-appflow-flow-destinationconnectorproperties-upsolver): 
    UpsolverDestinationProperties
```

## Properties<a name="aws-properties-appflow-flow-destinationconnectorproperties-properties"></a>

`EventBridge`  <a name="cfn-appflow-flow-destinationconnectorproperties-eventbridge"></a>
 The properties required to query Amazon EventBridge\.   
*Required*: No  
*Type*: [EventBridgeDestinationProperties](aws-properties-appflow-flow-eventbridgedestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Redshift`  <a name="cfn-appflow-flow-destinationconnectorproperties-redshift"></a>
 The properties required to query Amazon Redshift\.   
*Required*: No  
*Type*: [RedshiftDestinationProperties](aws-properties-appflow-flow-redshiftdestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-appflow-flow-destinationconnectorproperties-s3"></a>
 The properties required to query Amazon S3\.   
*Required*: No  
*Type*: [S3DestinationProperties](aws-properties-appflow-flow-s3destinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salesforce`  <a name="cfn-appflow-flow-destinationconnectorproperties-salesforce"></a>
 The properties required to query Salesforce\.   
*Required*: No  
*Type*: [SalesforceDestinationProperties](aws-properties-appflow-flow-salesforcedestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Snowflake`  <a name="cfn-appflow-flow-destinationconnectorproperties-snowflake"></a>
 The properties required to query Snowflake\.   
*Required*: No  
*Type*: [SnowflakeDestinationProperties](aws-properties-appflow-flow-snowflakedestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Upsolver`  <a name="cfn-appflow-flow-destinationconnectorproperties-upsolver"></a>
 The properties required to query Upsolver\.   
*Required*: No  
*Type*: [UpsolverDestinationProperties](aws-properties-appflow-flow-upsolverdestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-destinationconnectorproperties--seealso"></a>
+ [DestinationConnectorProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DestinationConnectorProperties.html) in the *Amazon AppFlow API Reference*\.


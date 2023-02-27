# AWS::AppFlow::Flow DestinationConnectorProperties<a name="aws-properties-appflow-flow-destinationconnectorproperties"></a>

 This stores the information that is required to query a particular connector\. 

## Syntax<a name="aws-properties-appflow-flow-destinationconnectorproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-destinationconnectorproperties-syntax.json"></a>

```
{
  "[CustomConnector](#cfn-appflow-flow-destinationconnectorproperties-customconnector)" : CustomConnectorDestinationProperties,
  "[EventBridge](#cfn-appflow-flow-destinationconnectorproperties-eventbridge)" : EventBridgeDestinationProperties,
  "[LookoutMetrics](#cfn-appflow-flow-destinationconnectorproperties-lookoutmetrics)" : LookoutMetricsDestinationProperties,
  "[Marketo](#cfn-appflow-flow-destinationconnectorproperties-marketo)" : MarketoDestinationProperties,
  "[Redshift](#cfn-appflow-flow-destinationconnectorproperties-redshift)" : RedshiftDestinationProperties,
  "[S3](#cfn-appflow-flow-destinationconnectorproperties-s3)" : S3DestinationProperties,
  "[Salesforce](#cfn-appflow-flow-destinationconnectorproperties-salesforce)" : SalesforceDestinationProperties,
  "[SAPOData](#cfn-appflow-flow-destinationconnectorproperties-sapodata)" : SAPODataDestinationProperties,
  "[Snowflake](#cfn-appflow-flow-destinationconnectorproperties-snowflake)" : SnowflakeDestinationProperties,
  "[Upsolver](#cfn-appflow-flow-destinationconnectorproperties-upsolver)" : UpsolverDestinationProperties,
  "[Zendesk](#cfn-appflow-flow-destinationconnectorproperties-zendesk)" : ZendeskDestinationProperties
}
```

### YAML<a name="aws-properties-appflow-flow-destinationconnectorproperties-syntax.yaml"></a>

```
  [CustomConnector](#cfn-appflow-flow-destinationconnectorproperties-customconnector): 
    CustomConnectorDestinationProperties
  [EventBridge](#cfn-appflow-flow-destinationconnectorproperties-eventbridge): 
    EventBridgeDestinationProperties
  [LookoutMetrics](#cfn-appflow-flow-destinationconnectorproperties-lookoutmetrics): 
    LookoutMetricsDestinationProperties
  [Marketo](#cfn-appflow-flow-destinationconnectorproperties-marketo): 
    MarketoDestinationProperties
  [Redshift](#cfn-appflow-flow-destinationconnectorproperties-redshift): 
    RedshiftDestinationProperties
  [S3](#cfn-appflow-flow-destinationconnectorproperties-s3): 
    S3DestinationProperties
  [Salesforce](#cfn-appflow-flow-destinationconnectorproperties-salesforce): 
    SalesforceDestinationProperties
  [SAPOData](#cfn-appflow-flow-destinationconnectorproperties-sapodata): 
    SAPODataDestinationProperties
  [Snowflake](#cfn-appflow-flow-destinationconnectorproperties-snowflake): 
    SnowflakeDestinationProperties
  [Upsolver](#cfn-appflow-flow-destinationconnectorproperties-upsolver): 
    UpsolverDestinationProperties
  [Zendesk](#cfn-appflow-flow-destinationconnectorproperties-zendesk): 
    ZendeskDestinationProperties
```

## Properties<a name="aws-properties-appflow-flow-destinationconnectorproperties-properties"></a>

`CustomConnector`  <a name="cfn-appflow-flow-destinationconnectorproperties-customconnector"></a>
The properties that are required to query the custom Connector\.  
*Required*: No  
*Type*: [CustomConnectorDestinationProperties](aws-properties-appflow-flow-customconnectordestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBridge`  <a name="cfn-appflow-flow-destinationconnectorproperties-eventbridge"></a>
 The properties required to query Amazon EventBridge\.   
*Required*: No  
*Type*: [EventBridgeDestinationProperties](aws-properties-appflow-flow-eventbridgedestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LookoutMetrics`  <a name="cfn-appflow-flow-destinationconnectorproperties-lookoutmetrics"></a>
 The properties required to query Amazon Lookout for Metrics\.   
*Required*: No  
*Type*: [LookoutMetricsDestinationProperties](aws-properties-appflow-flow-lookoutmetricsdestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Marketo`  <a name="cfn-appflow-flow-destinationconnectorproperties-marketo"></a>
The properties required to query Marketo\.  
*Required*: No  
*Type*: [MarketoDestinationProperties](aws-properties-appflow-flow-marketodestinationproperties.md)  
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

`SAPOData`  <a name="cfn-appflow-flow-destinationconnectorproperties-sapodata"></a>
The properties required to query SAPOData\.  
*Required*: No  
*Type*: [SAPODataDestinationProperties](aws-properties-appflow-flow-sapodatadestinationproperties.md)  
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

`Zendesk`  <a name="cfn-appflow-flow-destinationconnectorproperties-zendesk"></a>
The properties required to query Zendesk\.  
*Required*: No  
*Type*: [ZendeskDestinationProperties](aws-properties-appflow-flow-zendeskdestinationproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-destinationconnectorproperties--seealso"></a>
+ [DestinationConnectorProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DestinationConnectorProperties.html) in the *Amazon AppFlow API Reference*\.


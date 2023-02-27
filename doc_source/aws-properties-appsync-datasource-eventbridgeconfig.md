# AWS::AppSync::DataSource EventBridgeConfig<a name="aws-properties-appsync-datasource-eventbridgeconfig"></a>

The data source\. This can be an API destination, resource, or AWS service\.

## Syntax<a name="aws-properties-appsync-datasource-eventbridgeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-eventbridgeconfig-syntax.json"></a>

```
{
  "[EventBusArn](#cfn-appsync-datasource-eventbridgeconfig-eventbusarn)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-eventbridgeconfig-syntax.yaml"></a>

```
  [EventBusArn](#cfn-appsync-datasource-eventbridgeconfig-eventbusarn): String
```

## Properties<a name="aws-properties-appsync-datasource-eventbridgeconfig-properties"></a>

`EventBusArn`  <a name="cfn-appsync-datasource-eventbridgeconfig-eventbusarn"></a>
The event bus pipeline's ARN\. For more information about event buses, see [EventBridge event buses](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-bus.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
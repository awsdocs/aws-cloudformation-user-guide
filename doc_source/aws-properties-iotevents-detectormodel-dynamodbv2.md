# AWS::IoTEvents::DetectorModel DynamoDBv2<a name="aws-properties-iotevents-detectormodel-dynamodbv2"></a>

Defines an action to write to the Amazon DynamoDB table that you created\. The default action payload contains all attribute\-value pairs that have the information about the detector model instance and the event that triggered the action\. You can also customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. A separate column of the DynamoDB table receives one attribute\-value pair in the payload that you specify\.

**Important**  
The `type` value for `Payload` must be `JSON`\.

You can use expressions for parameters that are strings\. For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the *AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-properties-iotevents-detectormodel-dynamodbv2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-dynamodbv2-syntax.json"></a>

```
{
  "[Payload](#cfn-iotevents-detectormodel-dynamodbv2-payload)" : [Payload](aws-properties-iotevents-detectormodel-payload.md),
  "[TableName](#cfn-iotevents-detectormodel-dynamodbv2-tablename)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-dynamodbv2-syntax.yaml"></a>

```
  [Payload](#cfn-iotevents-detectormodel-dynamodbv2-payload): 
    [Payload](aws-properties-iotevents-detectormodel-payload.md)
  [TableName](#cfn-iotevents-detectormodel-dynamodbv2-tablename): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-dynamodbv2-properties"></a>

`Payload`  <a name="cfn-iotevents-detectormodel-dynamodbv2-payload"></a>
Information needed to configure the payload\.  
By default, AWS IoT Events generates a standard payload in JSON for any action\. This action payload contains all attribute\-value pairs that have the information about the detector model instance and the event triggered the action\. To configure the action payload, you can use `contentExpression`\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-detectormodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-iotevents-detectormodel-dynamodbv2-tablename"></a>
The name of the DynamoDB table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
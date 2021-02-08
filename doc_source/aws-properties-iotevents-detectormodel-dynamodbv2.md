# AWS::IoTEvents::DetectorModel DynamoDBv2<a name="aws-properties-iotevents-detectormodel-dynamodbv2"></a>

Defines an action to write to the Amazon DynamoDB table that you created\. The default action payload contains all the information about the detector model instance and the event that triggered the action\. You can customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. A separate column of the DynamoDB table receives one attribute\-value pair in the payload that you specify\.

You must use expressions for all parameters in `DynamoDBv2Action`\. The expressions accept literals, operators, functions, references, and substitution templates\.

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `tableName` parameter can be `'GreenhouseTemperatureTable'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `tableName` parameter can be `$variable.ddbtableName`\.
+ For a substitution template, you must use `${}`, and the template must be in single quotes\. A substitution template can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `contentExpression` parameter in `Payload` uses a substitution template\. 

   `'{\"sensorID\": \"${$input.GreenhouseInput.sensor_id}\", \"temperature\": \"${$input.GreenhouseInput.temperature * 9 / 5 + 32}\"}'` 
+ For a string concatenation, you must use `+`\. A string concatenation can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `tableName` parameter uses a string concatenation\. 

   `'GreenhouseTemperatureTable ' + $input.GreenhouseInput.date` 

For more information, see [Syntax](https://docs.aws.amazon.com/iotevents/latest/developerguide/expression-syntax.html) in the *AWS IoT Events Developer Guide*\.

The value for the `type` parameter in `Payload` must be `JSON`\.

## Syntax<a name="aws-properties-iotevents-detectormodel-dynamodbv2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-dynamodbv2-syntax.json"></a>

```
{
  "[Payload](#cfn-iotevents-detectormodel-dynamodbv2-payload)" : Payload,
  "[TableName](#cfn-iotevents-detectormodel-dynamodbv2-tablename)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-dynamodbv2-syntax.yaml"></a>

```
  [Payload](#cfn-iotevents-detectormodel-dynamodbv2-payload): 
    Payload
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
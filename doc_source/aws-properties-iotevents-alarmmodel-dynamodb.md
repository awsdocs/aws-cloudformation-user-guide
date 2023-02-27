# AWS::IoTEvents::AlarmModel DynamoDB<a name="aws-properties-iotevents-alarmmodel-dynamodb"></a>

Defines an action to write to the Amazon DynamoDB table that you created\. The standard action payload contains all the information about the detector model instance and the event that triggered the action\. You can customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. One column of the DynamoDB table receives all attribute\-value pairs in the payload that you specify\.

You must use expressions for all parameters in `DynamoDBAction`\. The expressions accept literals, operators, functions, references, and substitution templates\.

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `hashKeyType` parameter can be `'STRING'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `hashKeyField` parameter can be `$input.GreenhouseInput.name`\.
+ For a substitution template, you must use `${}`, and the template must be in single quotes\. A substitution template can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `hashKeyValue` parameter uses a substitution template\. 

   `'${$input.GreenhouseInput.temperature * 6 / 5 + 32} in Fahrenheit'` 
+ For a string concatenation, you must use `+`\. A string concatenation can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `tableName` parameter uses a string concatenation\. 

   `'GreenhouseTemperatureTable ' + $input.GreenhouseInput.date` 

For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the * AWS IoT Events Developer Guide*\.

If the defined payload type is a string, `DynamoDBAction` writes non\-JSON data to the DynamoDB table as binary data\. The DynamoDB console displays the data as Base64\-encoded text\. The value for the `payloadField` parameter is `<payload-field>_raw`\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-dynamodb-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-dynamodb-syntax.json"></a>

```
{
  "[HashKeyField](#cfn-iotevents-alarmmodel-dynamodb-hashkeyfield)" : String,
  "[HashKeyType](#cfn-iotevents-alarmmodel-dynamodb-hashkeytype)" : String,
  "[HashKeyValue](#cfn-iotevents-alarmmodel-dynamodb-hashkeyvalue)" : String,
  "[Operation](#cfn-iotevents-alarmmodel-dynamodb-operation)" : String,
  "[Payload](#cfn-iotevents-alarmmodel-dynamodb-payload)" : Payload,
  "[PayloadField](#cfn-iotevents-alarmmodel-dynamodb-payloadfield)" : String,
  "[RangeKeyField](#cfn-iotevents-alarmmodel-dynamodb-rangekeyfield)" : String,
  "[RangeKeyType](#cfn-iotevents-alarmmodel-dynamodb-rangekeytype)" : String,
  "[RangeKeyValue](#cfn-iotevents-alarmmodel-dynamodb-rangekeyvalue)" : String,
  "[TableName](#cfn-iotevents-alarmmodel-dynamodb-tablename)" : String
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-dynamodb-syntax.yaml"></a>

```
  [HashKeyField](#cfn-iotevents-alarmmodel-dynamodb-hashkeyfield): String
  [HashKeyType](#cfn-iotevents-alarmmodel-dynamodb-hashkeytype): String
  [HashKeyValue](#cfn-iotevents-alarmmodel-dynamodb-hashkeyvalue): String
  [Operation](#cfn-iotevents-alarmmodel-dynamodb-operation): String
  [Payload](#cfn-iotevents-alarmmodel-dynamodb-payload): 
    Payload
  [PayloadField](#cfn-iotevents-alarmmodel-dynamodb-payloadfield): String
  [RangeKeyField](#cfn-iotevents-alarmmodel-dynamodb-rangekeyfield): String
  [RangeKeyType](#cfn-iotevents-alarmmodel-dynamodb-rangekeytype): String
  [RangeKeyValue](#cfn-iotevents-alarmmodel-dynamodb-rangekeyvalue): String
  [TableName](#cfn-iotevents-alarmmodel-dynamodb-tablename): String
```

## Properties<a name="aws-properties-iotevents-alarmmodel-dynamodb-properties"></a>

`HashKeyField`  <a name="cfn-iotevents-alarmmodel-dynamodb-hashkeyfield"></a>
The name of the hash key \(also called the partition key\)\. The `hashKeyField` value must match the partition key of the target DynamoDB table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HashKeyType`  <a name="cfn-iotevents-alarmmodel-dynamodb-hashkeytype"></a>
The data type for the hash key \(also called the partition key\)\. You can specify the following values:  
+  `'STRING'` \- The hash key is a string\.
+  `'NUMBER'` \- The hash key is a number\.
If you don't specify `hashKeyType`, the default value is `'STRING'`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HashKeyValue`  <a name="cfn-iotevents-alarmmodel-dynamodb-hashkeyvalue"></a>
The value of the hash key \(also called the partition key\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operation`  <a name="cfn-iotevents-alarmmodel-dynamodb-operation"></a>
The type of operation to perform\. You can specify the following values:   
+  `'INSERT'` \- Insert data as a new item into the DynamoDB table\. This item uses the specified hash key as a partition key\. If you specified a range key, the item uses the range key as a sort key\.
+  `'UPDATE'` \- Update an existing item of the DynamoDB table with new data\. This item's partition key must match the specified hash key\. If you specified a range key, the range key must match the item's sort key\.
+  `'DELETE'` \- Delete an existing item of the DynamoDB table\. This item's partition key must match the specified hash key\. If you specified a range key, the range key must match the item's sort key\.
If you don't specify this parameter, AWS IoT Events triggers the `'INSERT'` operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Payload`  <a name="cfn-iotevents-alarmmodel-dynamodb-payload"></a>
Information needed to configure the payload\.  
By default, AWS IoT Events generates a standard payload in JSON for any action\. This action payload contains all attribute\-value pairs that have the information about the detector model instance and the event triggered the action\. To configure the action payload, you can use `contentExpression`\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-alarmmodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadField`  <a name="cfn-iotevents-alarmmodel-dynamodb-payloadfield"></a>
The name of the DynamoDB column that receives the action payload\.  
If you don't specify this parameter, the name of the DynamoDB column is `payload`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeKeyField`  <a name="cfn-iotevents-alarmmodel-dynamodb-rangekeyfield"></a>
The name of the range key \(also called the sort key\)\. The `rangeKeyField` value must match the sort key of the target DynamoDB table\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeKeyType`  <a name="cfn-iotevents-alarmmodel-dynamodb-rangekeytype"></a>
The data type for the range key \(also called the sort key\), You can specify the following values:  
+  `'STRING'` \- The range key is a string\.
+  `'NUMBER'` \- The range key is number\.
If you don't specify `rangeKeyField`, the default value is `'STRING'`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeKeyValue`  <a name="cfn-iotevents-alarmmodel-dynamodb-rangekeyvalue"></a>
The value of the range key \(also called the sort key\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-iotevents-alarmmodel-dynamodb-tablename"></a>
The name of the DynamoDB table\. The `tableName` value must match the table name of the target DynamoDB table\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::IoT::TopicRule DynamoDBAction<a name="aws-properties-iot-topicrule-dynamodbaction"></a>

Describes an action to write to a DynamoDB table\.

The `tableName`, `hashKeyField`, and `rangeKeyField` values must match the values used when you created the table\.

The `hashKeyValue` and `rangeKeyvalue` fields use a substitution template syntax\. These templates provide data at runtime\. The syntax is as follows: $\{*sql\-expression*\}\.

You can specify any valid expression in a WHERE or SELECT clause, including JSON properties, comparisons, calculations, and functions\. For example, the following field uses the third level of the topic:

 `"hashKeyValue": "${topic(3)}"` 

The following field uses the timestamp:

 `"rangeKeyValue": "${timestamp()}"` 

For more information, see [DynamoDBv2 Action](https://docs.aws.amazon.com/iot/latest/developerguide/iot-rule-actions.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-properties-iot-topicrule-dynamodbaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-dynamodbaction-syntax.json"></a>

```
{
  "[HashKeyField](#cfn-iot-topicrule-dynamodbaction-hashkeyfield)" : String,
  "[HashKeyType](#cfn-iot-topicrule-dynamodbaction-hashkeytype)" : String,
  "[HashKeyValue](#cfn-iot-topicrule-dynamodbaction-hashkeyvalue)" : String,
  "[PayloadField](#cfn-iot-topicrule-dynamodbaction-payloadfield)" : String,
  "[RangeKeyField](#cfn-iot-topicrule-dynamodbaction-rangekeyfield)" : String,
  "[RangeKeyType](#cfn-iot-topicrule-dynamodbaction-rangekeytype)" : String,
  "[RangeKeyValue](#cfn-iot-topicrule-dynamodbaction-rangekeyvalue)" : String,
  "[RoleArn](#cfn-iot-topicrule-dynamodbaction-rolearn)" : String,
  "[TableName](#cfn-iot-topicrule-dynamodbaction-tablename)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-dynamodbaction-syntax.yaml"></a>

```
  [HashKeyField](#cfn-iot-topicrule-dynamodbaction-hashkeyfield): String
  [HashKeyType](#cfn-iot-topicrule-dynamodbaction-hashkeytype): String
  [HashKeyValue](#cfn-iot-topicrule-dynamodbaction-hashkeyvalue): String
  [PayloadField](#cfn-iot-topicrule-dynamodbaction-payloadfield): String
  [RangeKeyField](#cfn-iot-topicrule-dynamodbaction-rangekeyfield): String
  [RangeKeyType](#cfn-iot-topicrule-dynamodbaction-rangekeytype): String
  [RangeKeyValue](#cfn-iot-topicrule-dynamodbaction-rangekeyvalue): String
  [RoleArn](#cfn-iot-topicrule-dynamodbaction-rolearn): String
  [TableName](#cfn-iot-topicrule-dynamodbaction-tablename): String
```

## Properties<a name="aws-properties-iot-topicrule-dynamodbaction-properties"></a>

`HashKeyField`  <a name="cfn-iot-topicrule-dynamodbaction-hashkeyfield"></a>
The hash key name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HashKeyType`  <a name="cfn-iot-topicrule-dynamodbaction-hashkeytype"></a>
The hash key type\. Valid values are "STRING" or "NUMBER"  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HashKeyValue`  <a name="cfn-iot-topicrule-dynamodbaction-hashkeyvalue"></a>
The hash key value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadField`  <a name="cfn-iot-topicrule-dynamodbaction-payloadfield"></a>
The action payload\. This name can be customized\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeKeyField`  <a name="cfn-iot-topicrule-dynamodbaction-rangekeyfield"></a>
The range key name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeKeyType`  <a name="cfn-iot-topicrule-dynamodbaction-rangekeytype"></a>
The range key type\. Valid values are "STRING" or "NUMBER"  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeKeyValue`  <a name="cfn-iot-topicrule-dynamodbaction-rangekeyvalue"></a>
The range key value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-dynamodbaction-rolearn"></a>
The ARN of the IAM role that grants access to the DynamoDB table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-iot-topicrule-dynamodbaction-tablename"></a>
The name of the DynamoDB table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
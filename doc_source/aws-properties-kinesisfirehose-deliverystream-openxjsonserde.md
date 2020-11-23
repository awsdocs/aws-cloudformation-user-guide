# AWS::KinesisFirehose::DeliveryStream OpenXJsonSerDe<a name="aws-properties-kinesisfirehose-deliverystream-openxjsonserde"></a>

The OpenX SerDe\. Used by Kinesis Data Firehose for deserializing data, which means converting it from the JSON format in preparation for serializing it to the Parquet or ORC format\. This is one of two deserializers you can choose, depending on which one offers the functionality you need\. The other option is the native Hive / HCatalog JsonSerDe\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-openxjsonserde-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-openxjsonserde-syntax.json"></a>

```
{
  "[CaseInsensitive](#cfn-kinesisfirehose-deliverystream-openxjsonserde-caseinsensitive)" : Boolean,
  "[ColumnToJsonKeyMappings](#cfn-kinesisfirehose-deliverystream-openxjsonserde-columntojsonkeymappings)" : {Key : Value, ...},
  "[ConvertDotsInJsonKeysToUnderscores](#cfn-kinesisfirehose-deliverystream-openxjsonserde-convertdotsinjsonkeystounderscores)" : Boolean
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-openxjsonserde-syntax.yaml"></a>

```
  [CaseInsensitive](#cfn-kinesisfirehose-deliverystream-openxjsonserde-caseinsensitive): Boolean
  [ColumnToJsonKeyMappings](#cfn-kinesisfirehose-deliverystream-openxjsonserde-columntojsonkeymappings): 
    Key : Value
  [ConvertDotsInJsonKeysToUnderscores](#cfn-kinesisfirehose-deliverystream-openxjsonserde-convertdotsinjsonkeystounderscores): Boolean
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-openxjsonserde-properties"></a>

`CaseInsensitive`  <a name="cfn-kinesisfirehose-deliverystream-openxjsonserde-caseinsensitive"></a>
When set to `true`, which is the default, Kinesis Data Firehose converts JSON keys to lowercase before deserializing them\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnToJsonKeyMappings`  <a name="cfn-kinesisfirehose-deliverystream-openxjsonserde-columntojsonkeymappings"></a>
Maps column names to JSON keys that aren't identical to the column names\. This is useful when the JSON contains keys that are Hive keywords\. For example, `timestamp` is a Hive keyword\. If you have a JSON key named `timestamp`, set this parameter to `{"ts": "timestamp"}` to map this key to a column named `ts`\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConvertDotsInJsonKeysToUnderscores`  <a name="cfn-kinesisfirehose-deliverystream-openxjsonserde-convertdotsinjsonkeystounderscores"></a>
When set to `true`, specifies that the names of the keys include dots and that you want Kinesis Data Firehose to replace them with underscores\. This is useful because Apache Hive does not allow dots in column names\. For example, if the JSON contains a key whose name is "a\.b", you can define the column name to be "a\_b" when using this option\.  
The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
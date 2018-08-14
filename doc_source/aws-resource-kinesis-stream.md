# AWS::Kinesis::Stream<a name="aws-resource-kinesis-stream"></a>

Creates an Kinesis stream that captures and transports data records that are emitted from data sources\. For information about creating streams, see [CreateStream](http://docs.aws.amazon.com/kinesis/latest/APIReference/API_CreateStream.html) in the *Amazon Kinesis API Reference*\.

**Topics**
+ [Syntax](#aws-resource-kinesis-stream-syntax)
+ [Properties](#w3ab2c21c10d820b9)
+ [Return Values](#w3ab2c21c10d820c11)
+ [Example](#aws-resource-kinesis-stream-examples)

## Syntax<a name="aws-resource-kinesis-stream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesis-stream-syntax.json"></a>

```
{
   "Type" : "AWS::Kinesis::Stream",
   "Properties" : {
      "[Name](#cfn-kinesis-stream-name)" : String,
      "[RetentionPeriodHours](#cfn-kinesis-stream-retentionperiodhours)" : Integer,
      "[ShardCount](#cfn-kinesis-stream-shardcount)" : Integer,
      "[StreamEncryption](#cfn-kinesis-stream-streamencryption)" : [Kinesis StreamEncryption](aws-properties-kinesis-stream-streamencryption.md),
      "[Tags](#cfn-kinesis-stream-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-kinesis-stream-syntax.yaml"></a>

```
Type: "AWS::Kinesis::Stream"
Properties: 
  [Name](#cfn-kinesis-stream-name): String
  [RetentionPeriodHours](#cfn-kinesis-stream-retentionperiodhours): Integer
  [ShardCount](#cfn-kinesis-stream-shardcount): Integer
  [StreamEncryption](#cfn-kinesis-stream-streamencryption): [Kinesis StreamEncryption](aws-properties-kinesis-stream-streamencryption.md)
  [Tags](#cfn-kinesis-stream-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d820b9"></a>

**Note**  
 For more information about constraints and values for each property, see [CreateStream](http://docs.aws.amazon.com/kinesis/latest/APIReference/API_CreateStream.html) in the *Amazon Kinesis API Reference* and [Amazon Kinesis Data Streams Limits](http://docs.aws.amazon.com/kinesis/latest/dev/service-sizes-and-limits.html) in the *Amazon Kinesis Developer Guide*\. 

`Name`  <a name="cfn-kinesis-stream-name"></a>
The name of the Kinesis stream\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the stream name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RetentionPeriodHours`  <a name="cfn-kinesis-stream-retentionperiodhours"></a>
The number of hours for the data records that are stored in shards to remain accessible\. The default value is 24\. For more information about the stream retention period, see [Changing the Data Retention Period](http://docs.aws.amazon.com/kinesis/latest/dev/kinesis-extended-retention.html) in the *Amazon Kinesis Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ShardCount`  <a name="cfn-kinesis-stream-shardcount"></a>
The number of shards that the stream uses\. For greater provisioned throughput, increase the number of shards\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StreamEncryption`  <a name="cfn-kinesis-stream-streamencryption"></a>
Enables or updates server\-side encryption using an AWS KMS key for a specified stream\.  
*Required*: No  
*Type:* [Kinesis StreamEncryption](aws-properties-kinesis-stream-streamencryption.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-kinesis-stream-tags"></a>
An arbitrary set of tags \(key–value pairs\) to associate with the Kinesis stream\. For information about constraints for this property, see [Tag Restrictions](http://docs.aws.amazon.com/kinesis/latest/dev/tagging.html#tagging-restrictions) in the *Amazon Kinesis Developer Guide*\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d820c11"></a>

### Ref<a name="w3ab2c21c10d820c11b2"></a>

 When you specify an AWS::Kinesis::Stream resource as an argument to the `Ref` function, AWS CloudFormation returns the stream name \(physical ID\)\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d820c11b4"></a>

`Fn::GetAtt` returns a value for the `Arn` attribute\.

`Arn`  
The Amazon resource name \(ARN\) of the Kinesis stream, such as `arn:aws:kinesis:``us-east-2``:123456789012:stream/mystream`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-kinesis-stream-examples"></a>

The following example creates a `Stream` resource that uses three shards, sets a seven\-day retention period, and specifies the KMS key for server\-side encryption\.

### JSON<a name="aws-resource-kinesis-stream-examples.json"></a>

```
"MyStream": {
  "Type": "AWS::Kinesis::Stream",
  "Properties": {
    "Name": "MyKinesisStream",
    "RetentionPeriodHours" : 168,
    "ShardCount": 3,
    "StreamEncryption": 
      {
        "EncryptionType": "KMS",
        "KeyId": "!Ref myKey"
      },
    "Tags": [
      {
        "Key": "Environment",
        "Value": "Production"
      }
   ]
  }
}
```

### YAML<a name="aws-resource-kinesis-stream-examples.yaml"></a>

```
MyStream:
  Type: 'AWS::Kinesis::Stream'
  Properties:
    Name: MyKinesisStream
    RetentionPeriodHours: 168
    ShardCount: 3
    StreamEncryption:
        EncryptionType: KMS
        KeyId: !Ref myKey
    Tags:
      -
        Key: Environment
        Value: Production
```
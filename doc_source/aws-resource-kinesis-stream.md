# AWS::Kinesis::Stream<a name="aws-resource-kinesis-stream"></a>

Creates a Kinesis stream that captures and transports data records that are emitted from data sources\. For information about creating streams, see [CreateStream](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_CreateStream.html) in the Amazon Kinesis API Reference\. 

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
      "[StreamEncryption](#cfn-kinesis-stream-streamencryption)" : StreamEncryption,
      "[Tags](#cfn-kinesis-stream-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-kinesis-stream-syntax.yaml"></a>

```
Type: AWS::Kinesis::Stream
Properties: 
  [Name](#cfn-kinesis-stream-name): String
  [RetentionPeriodHours](#cfn-kinesis-stream-retentionperiodhours): Integer
  [ShardCount](#cfn-kinesis-stream-shardcount): Integer
  [StreamEncryption](#cfn-kinesis-stream-streamencryption): 
    StreamEncryption
  [Tags](#cfn-kinesis-stream-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-kinesis-stream-properties"></a>

`Name`  <a name="cfn-kinesis-stream-name"></a>
The name of the Kinesis stream\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the stream name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.   
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RetentionPeriodHours`  <a name="cfn-kinesis-stream-retentionperiodhours"></a>
The number of hours for the data records that are stored in shards to remain accessible\. The default value is 24\. For more information about the stream retention period, see [Changing the Data Retention Period](https://docs.aws.amazon.com/streams/latest/dev/kinesis-extended-retention.html) in the Amazon Kinesis Developer Guide\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShardCount`  <a name="cfn-kinesis-stream-shardcount"></a>
The number of shards that the stream uses\. For greater provisioned throughput, increase the number of shards\.   
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamEncryption`  <a name="cfn-kinesis-stream-streamencryption"></a>
When specified, enables or updates server\-side encryption using an AWS KMS key for a specified stream\. Removing this property from your stack template and updating your stack disables encryption\.  
*Required*: No  
*Type*: [StreamEncryption](aws-properties-kinesis-stream-streamencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-kinesis-stream-tags"></a>
An arbitrary set of tags \(key–value pairs\) to associate with the Kinesis stream\. For information about constraints for this property, see [Tag Restrictions](https://docs.aws.amazon.com/streams/latest/dev/tagging.html#tagging-restrictions) in the *Amazon Kinesis Developer Guide*\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-kinesis-stream-return-values"></a>

### Ref<a name="aws-resource-kinesis-stream-return-values-ref"></a>

 When you specify an AWS::Kinesis::Stream resource as an argument to the `Ref` function, AWS CloudFormation returns the stream name \(physical ID\)\.

For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-kinesis-stream-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for the `Arn` attribute\.

For more information about using Fn::GetAtt, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-kinesis-stream-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon resource name \(ARN\) of the Kinesis stream, such as `arn:aws:kinesis:us-east-2:123456789012:stream/mystream`\.

## Examples<a name="aws-resource-kinesis-stream--examples"></a>



### Create a Stream<a name="aws-resource-kinesis-stream--examples--Create_a_Stream"></a>

The following example creates a `Stream` resource that uses three shards, sets a seven\-day retention period, and specifies the KMS key for server\-side encryption\.

#### JSON<a name="aws-resource-kinesis-stream--examples--Create_a_Stream--json"></a>

```
"MyStream": { 
    "Type": "AWS::Kinesis::Stream", 
    "Properties": {
        "Name": "MyKinesisStream", 
        "RetentionPeriodHours" : 168, 
        "ShardCount": 3,
        "StreamEncryption": { 
            "EncryptionType": "KMS", 
            "KeyId": "!Ref myKey" 
            }, 
        "Tags": [ {
            "Key": "Environment", 
            "Value": "Production" } ] 
        } 
}
```

#### YAML<a name="aws-resource-kinesis-stream--examples--Create_a_Stream--yaml"></a>

```
MyStream: 
    Type: AWS::Kinesis::Stream 
    Properties: 
        Name: MyKinesisStream 
        RetentionPeriodHours: 168 
        ShardCount: 3 
        StreamEncryption:
            EncryptionType: KMS 
            KeyId: !Ref myKey 
        Tags: 
            -
                Key: Environment Value:
                Production
```
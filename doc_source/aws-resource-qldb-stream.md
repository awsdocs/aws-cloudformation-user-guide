# AWS::QLDB::Stream<a name="aws-resource-qldb-stream"></a>

The `AWS::QLDB::Stream` resource creates a journal stream for a given Amazon Quantum Ledger Database \(Amazon QLDB\) ledger\. The stream captures every document revision that is committed to the ledger's journal and delivers the data to a specified Amazon Kinesis Data Streams resource\.

For more information, see [StreamJournalToKinesis](https://docs.aws.amazon.com/qldb/latest/developerguide/API_StreamJournalToKinesis.html) in the *Amazon QLDB API Reference*\.

## Syntax<a name="aws-resource-qldb-stream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-qldb-stream-syntax.json"></a>

```
{
  "Type" : "AWS::QLDB::Stream",
  "Properties" : {
      "[ExclusiveEndTime](#cfn-qldb-stream-exclusiveendtime)" : String,
      "[InclusiveStartTime](#cfn-qldb-stream-inclusivestarttime)" : String,
      "[KinesisConfiguration](#cfn-qldb-stream-kinesisconfiguration)" : KinesisConfiguration,
      "[LedgerName](#cfn-qldb-stream-ledgername)" : String,
      "[RoleArn](#cfn-qldb-stream-rolearn)" : String,
      "[StreamName](#cfn-qldb-stream-streamname)" : String,
      "[Tags](#cfn-qldb-stream-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-qldb-stream-syntax.yaml"></a>

```
Type: AWS::QLDB::Stream
Properties: 
  [ExclusiveEndTime](#cfn-qldb-stream-exclusiveendtime): String
  [InclusiveStartTime](#cfn-qldb-stream-inclusivestarttime): String
  [KinesisConfiguration](#cfn-qldb-stream-kinesisconfiguration): 
    KinesisConfiguration
  [LedgerName](#cfn-qldb-stream-ledgername): String
  [RoleArn](#cfn-qldb-stream-rolearn): String
  [StreamName](#cfn-qldb-stream-streamname): String
  [Tags](#cfn-qldb-stream-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-qldb-stream-properties"></a>

`ExclusiveEndTime`  <a name="cfn-qldb-stream-exclusiveendtime"></a>
The exclusive date and time that specifies when the stream ends\. If you don't define this parameter, the stream runs indefinitely until you cancel it\.  
The `ExclusiveEndTime` must be in `ISO 8601` date and time format and in Universal Coordinated Time \(UTC\)\. For example: `2019-06-13T21:36:34Z`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InclusiveStartTime`  <a name="cfn-qldb-stream-inclusivestarttime"></a>
The inclusive start date and time from which to start streaming journal data\. This parameter must be in `ISO 8601` date and time format and in Universal Coordinated Time \(UTC\)\. For example: `2019-06-13T21:36:34Z`\.  
The `InclusiveStartTime` cannot be in the future and must be before `ExclusiveEndTime`\.  
If you provide an `InclusiveStartTime` that is before the ledger's `CreationDateTime`, QLDB effectively defaults it to the ledger's `CreationDateTime`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KinesisConfiguration`  <a name="cfn-qldb-stream-kinesisconfiguration"></a>
The configuration settings of the Kinesis Data Streams destination for your stream request\.  
*Required*: Yes  
*Type*: [KinesisConfiguration](aws-properties-qldb-stream-kinesisconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LedgerName`  <a name="cfn-qldb-stream-ledgername"></a>
The name of the ledger\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `(?!^.*--)(?!^[0-9]+$)(?!^-)(?!.*-$)^[A-Za-z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-qldb-stream-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that grants QLDB permissions for a journal stream to write data records to a Kinesis Data Streams resource\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `1600`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StreamName`  <a name="cfn-qldb-stream-streamname"></a>
The name that you want to assign to the QLDB journal stream\. User\-defined names can help identify and indicate the purpose of a stream\.  
Your stream name must be unique among other *active* streams for a given ledger\. Stream names have the same naming constraints as ledger names, as defined in [Quotas in Amazon QLDB](https://docs.aws.amazon.com/qldb/latest/developerguide/limits.html#limits.naming) in the *Amazon QLDB Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `(?!^.*--)(?!^[0-9]+$)(?!^-)(?!.*-$)^[A-Za-z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-qldb-stream-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-qldb-stream-return-values"></a>

### Ref<a name="aws-resource-qldb-stream-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID or ARN\. For example:

 `{ "Ref": "myQLDBStream" }` 

For the resource with the logical ID `myQLDBStream`, `Ref` returns the ID or ARN of the Amazon QLDB journal stream\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-qldb-stream-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-qldb-stream-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the QLDB journal stream\. For example: `arn:aws:qldb:us-east-1:123456789012:stream/exampleLedger/IiPT4brpZCqCq3f4MTHbYy`\.

`Id`  <a name="Id-fn::getatt"></a>
The unique ID that QLDB assigns to each QLDB journal stream\. For example: `IiPT4brpZCqCq3f4MTHbYy`\.

## Examples<a name="aws-resource-qldb-stream--examples"></a>



### Amazon QLDB Stream<a name="aws-resource-qldb-stream--examples--Amazon_QLDB_Stream"></a>

The following example describes an Amazon QLDB journal stream for a ledger named `exampleLedger` and a Kinesis Data Streams destination with the ARN `arn:aws:kinesis:us-east-1:123456789012:stream/stream-for-qldb`\.

#### JSON<a name="aws-resource-qldb-stream--examples--Amazon_QLDB_Stream--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myQLDBStream": {
      "Type": "AWS::QLDB::Stream",
      "Properties": {
        "ExclusiveEndTime" : "2020-05-29T22:59:59Z",
        "InclusiveStartTime" : "2020-05-29T00:00:00Z",
        "KinesisConfiguration" : {
          "AggregationEnabled": true,
          "StreamArn": "arn:aws:kinesis:us-east-1:123456789012:stream/stream-for-qldb"
        },
        "LedgerName" : "exampleLedger",
        "RoleArn" : "arn:aws:iam::123456789012:role/my-kinesis-stream-role",
        "StreamName" : "exampleLedger-stream",
        "Tags": [
          {
            "Key": "Domain",
            "Value": "Test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-qldb-stream--examples--Amazon_QLDB_Stream--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  myQLDBStream:
    Type: "AWS::QLDB::Stream"
    Properties:
      ExclusiveEndTime: "2020-05-29T22:59:59Z"
      InclusiveStartTime: "2020-05-29T00:00:00Z"
      KinesisConfiguration:
        AggregationEnabled: true
        StreamArn: "arn:aws:kinesis:us-east-1:123456789012:stream/stream-for-qldb"
      LedgerName: "exampleLedger"
      RoleArn: "arn:aws:iam::123456789012:role/my-kinesis-stream-role"
      StreamName: "exampleLedger-stream"
      Tags:
        - Key: Domain
          Value: Test
```

## See also<a name="aws-resource-qldb-stream--seealso"></a>
+  [StreamJournalToKinesis](https://docs.aws.amazon.com/qldb/latest/developerguide/API_StreamJournalToKinesis.html) in the *Amazon QLDB API Reference*


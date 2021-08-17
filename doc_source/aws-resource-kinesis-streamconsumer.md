# AWS::Kinesis::StreamConsumer<a name="aws-resource-kinesis-streamconsumer"></a>

Use the AWS CloudFormation `AWS::Kinesis::StreamConsumer` resource to register a consumer with a Kinesis data stream\. The consumer you register can then call [SubscribeToShard](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_SubscribeToShard.html) to receive data from the stream using enhanced fan\-out, at a rate of up to 2 MiB per second for every shard you subscribe to\. This rate is unaffected by the total number of consumers that read from the same stream\. 

You can register up to five consumers per stream\. However, you can request a limit increase using the [Kinesis Data Streams limits form](https://console.aws.amazon.com/support/v1?#/)\. A given consumer can only be registered with one stream at a time\. 

For more information, see [Using Consumers with Enhanced Fan\-Out](https://docs.aws.amazon.com/streams/latest/dev/introduction-to-enhanced-consumers.html)\. 

## Syntax<a name="aws-resource-kinesis-streamconsumer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesis-streamconsumer-syntax.json"></a>

```
{
  "Type" : "AWS::Kinesis::StreamConsumer",
  "Properties" : {
      "[ConsumerName](#cfn-kinesis-streamconsumer-consumername)" : String,
      "[StreamARN](#cfn-kinesis-streamconsumer-streamarn)" : String
    }
}
```

### YAML<a name="aws-resource-kinesis-streamconsumer-syntax.yaml"></a>

```
Type: AWS::Kinesis::StreamConsumer
Properties: 
  [ConsumerName](#cfn-kinesis-streamconsumer-consumername): String
  [StreamARN](#cfn-kinesis-streamconsumer-streamarn): String
```

## Properties<a name="aws-resource-kinesis-streamconsumer-properties"></a>

`ConsumerName`  <a name="cfn-kinesis-streamconsumer-consumername"></a>
The name of the consumer is something you choose when you register the consumer\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StreamARN`  <a name="cfn-kinesis-streamconsumer-streamarn"></a>
The ARN of the stream with which you registered the consumer\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:aws.*:kinesis:.*:\d{12}:stream/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-kinesis-streamconsumer-return-values"></a>

### Ref<a name="aws-resource-kinesis-streamconsumer-return-values-ref"></a>

When you pass the logical ID of an `AWS::Kinesis::StreamConsumer` resource to the intrinsic Ref function, the function returns the consumer ARN\. For example ARN formats, see [Example ARNs](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html#arns-syntax)\. 

For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-kinesis-streamconsumer-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using Fn::GetAtt, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-kinesis-streamconsumer-return-values-fn--getatt-fn--getatt"></a>

`ConsumerARN`  <a name="ConsumerARN-fn::getatt"></a>
When you register a consumer, Kinesis Data Streams generates an ARN for it\. You need this ARN to be able to call [SubscribeToShard](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_SubscribeToShard.html)\.   
If you delete a consumer and then create a new one with the same name, it won't have the same ARN\. That's because consumer ARNs contain the creation timestamp\. This is important to keep in mind if you have IAM policies that reference consumer ARNs\. 

`ConsumerCreationTimestamp`  <a name="ConsumerCreationTimestamp-fn::getatt"></a>
The time at which the consumer was created\.

`ConsumerName`  <a name="ConsumerName-fn::getatt"></a>
The name you gave the consumer when you registered it\.

`ConsumerStatus`  <a name="ConsumerStatus-fn::getatt"></a>
A consumer can't read data while in the `CREATING` or `DELETING` states\.

`StreamARN`  <a name="StreamARN-fn::getatt"></a>
The ARN of the data stream with which the consumer is registered\.

## Examples<a name="aws-resource-kinesis-streamconsumer--examples"></a>



### Register a Consumer with a Kinesis Data Stream<a name="aws-resource-kinesis-streamconsumer--examples--Register_a_Consumer_with_a_Kinesis_Data_Stream"></a>



#### JSON<a name="aws-resource-kinesis-streamconsumer--examples--Register_a_Consumer_with_a_Kinesis_Data_Stream--json"></a>

```
{ 
    "Parameters": { 
        "TestStreamARN": { 
            "Type": "String" },
        "TestConsumerName": { 
            "Type": "String" } }, 
    "Resources": { 
        "StreamConsumer": {
            "Type": "AWS::Kinesis::StreamConsumer", 
            "Properties": { 
                "StreamARN": { "Ref" : TestStreamARN }, 
                "ConsumerName": { "Ref" : TestConsumerName } 
                } 
        } 
   } 
}
```

#### YAML<a name="aws-resource-kinesis-streamconsumer--examples--Register_a_Consumer_with_a_Kinesis_Data_Stream--yaml"></a>

```
    Parameters: 
        TestStreamARN: 
            Type: String 
        TestConsumerName:
            Type: String 
            
    Resources: StreamConsumer: 
        Type: "AWS::Kinesis::StreamConsumer"
        Properties: 
            StreamARN: !Ref TestStreamARN 
            ConsumerName: !Ref TestConsumerName
```
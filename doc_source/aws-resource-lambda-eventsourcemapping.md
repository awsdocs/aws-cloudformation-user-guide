# AWS::Lambda::EventSourceMapping<a name="aws-resource-lambda-eventsourcemapping"></a>

The `AWS::Lambda::EventSourceMapping` resource creates a mapping between an event source and an AWS Lambda function\. Lambda reads items from the event source and triggers the function\. For more information, see [AWS Lambda Event Source Mapping](https://docs.aws.amazon.com/lambda/latest/dg/intro-invocation-modes.html) in the *AWS Lambda Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-lambda-eventsourcemapping-syntax)
+ [Properties](#w4ab1c21c10d162c13b9)
+ [Return Values](#w4ab1c21c10d162c13c11)
+ [Example](#w4ab1c21c10d162c13c13)

## Syntax<a name="aws-resource-lambda-eventsourcemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-eventsourcemapping-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::EventSourceMapping",
  "Properties" : {
    "[BatchSize](#cfn-lambda-eventsourcemapping-batchsize)" : Integer,
    "[Enabled](#cfn-lambda-eventsourcemapping-enabled)" : Boolean,
    "[EventSourceArn](#cfn-lambda-eventsourcemapping-eventsourcearn)" : String,
    "[FunctionName](#cfn-lambda-eventsourcemapping-functionname)" : String,
    "[StartingPosition](#cfn-lambda-eventsourcemapping-startingposition)" : String
  }
}
```

### YAML<a name="aws-resource-lambda-eventsourcemapping-syntax.yaml"></a>

```
Type: AWS::Lambda::EventSourceMapping
Properties: 
  [BatchSize](#cfn-lambda-eventsourcemapping-batchsize): Integer
  [Enabled](#cfn-lambda-eventsourcemapping-enabled): Boolean
  [EventSourceArn](#cfn-lambda-eventsourcemapping-eventsourcearn): String
  [FunctionName](#cfn-lambda-eventsourcemapping-functionname): String
  [StartingPosition](#cfn-lambda-eventsourcemapping-startingposition): String
```

## Properties<a name="w4ab1c21c10d162c13b9"></a>

`BatchSize`  <a name="cfn-lambda-eventsourcemapping-batchsize"></a>
The maximum number of items to retrieve in a single batch\.  
+ **Amazon Kinesis** – Default 100\. Max 10,000\.
+ **Amazon DynamoDB Streams** – Default 100\. Max 1,000\.
+ **Amazon Simple Queue Service** – Default 10\. Max 10\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Enabled`  <a name="cfn-lambda-eventsourcemapping-enabled"></a>
Disables the event source mapping to pause polling and invocation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EventSourceArn`  <a name="cfn-lambda-eventsourcemapping-eventsourcearn"></a>
The Amazon Resource Name \(ARN\) of the event source\.  
+ **Amazon Kinesis** – The ARN of the data stream or a stream consumer\.
+ **Amazon DynamoDB Streams** – The ARN of the stream\.
+ **Amazon Simple Queue Service** – The ARN of the queue\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`FunctionName`  <a name="cfn-lambda-eventsourcemapping-functionname"></a>
The name of the Lambda function\.  

**Name formats**
+ **Function name** \- `MyFunction`\.
+ **Function ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:MyFunction`\.
+ **Version or Alias ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:MyFunction:PROD`\.
+ **Partial ARN** \- `123456789012:function:MyFunction`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StartingPosition`  <a name="cfn-lambda-eventsourcemapping-startingposition"></a>
The position in a stream from which to start reading\. Required for Amazon Kinesis and Amazon DynamoDB Streams sources\. `AT_TIMESTAMP` is only supported for Kinesis streams\.   
Valid Values: `TRIM_HORIZON` \| `LATEST` \| `AT_TIMESTAMP`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w4ab1c21c10d162c13c11"></a>

### Ref<a name="w4ab1c21c10d162c13c11b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w4ab1c21c10d162c13c13"></a>

The following example associates an Kinesis stream with a Lambda function\.

### JSON<a name="aws-resource-lambda-eventsourcemapping-example.json"></a>

```
"EventSourceMapping": {  
  "Type": "AWS::Lambda::EventSourceMapping",
  "Properties": {
    "EventSourceArn" : { "Fn::Join" : [ "", [ "arn:aws:kinesis:", { "Ref" : "AWS::Region" }, ":", { "Ref" : "AWS::AccountId" }, ":stream/", { "Ref" : "KinesisStream" }] ] },
    "FunctionName" : { "Fn::GetAtt" : ["LambdaFunction", "Arn"] },
    "StartingPosition" : "TRIM_HORIZON"
  }
}
```

### YAML<a name="aws-resource-lambda-eventsourcemapping-example.yaml"></a>

```
EventSourceMapping: 
  Type: AWS::Lambda::EventSourceMapping
  Properties: 
    EventSourceArn: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:kinesis:"
          - 
            Ref: "AWS::Region"
          - ":"
          - 
            Ref: "AWS::AccountId"
          - ":stream/"
          - 
            Ref: "KinesisStream"
    FunctionName: 
      Fn::GetAtt: 
        - "LambdaFunction"
        - "Arn"
    StartingPosition: "TRIM_HORIZON"
```
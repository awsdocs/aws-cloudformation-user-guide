# AWS::Lambda::EventSourceMapping<a name="aws-resource-lambda-eventsourcemapping"></a>

The `AWS::Lambda::EventSourceMapping` resource creates a mapping between an event source and an AWS Lambda function\. Lambda reads items from the event source and triggers the function\.

For details about each event source type, see the following topics\.
+  [Using AWS Lambda with Amazon Kinesis](https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html) 
+  [Using AWS Lambda with Amazon SQS](https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html) 
+  [Using AWS Lambda with Amazon DynamoDB](https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html) 
+  [Using AWS Lambda with Amazon MSK](https://docs.aws.amazon.com/lambda/latest/dg/with-msk.html) 

## Syntax<a name="aws-resource-lambda-eventsourcemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-eventsourcemapping-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::EventSourceMapping",
  "Properties" : {
      "[BatchSize](#cfn-lambda-eventsourcemapping-batchsize)" : Integer,
      "[BisectBatchOnFunctionError](#cfn-lambda-eventsourcemapping-bisectbatchonfunctionerror)" : Boolean,
      "[DestinationConfig](#cfn-lambda-eventsourcemapping-destinationconfig)" : DestinationConfig,
      "[Enabled](#cfn-lambda-eventsourcemapping-enabled)" : Boolean,
      "[EventSourceArn](#cfn-lambda-eventsourcemapping-eventsourcearn)" : String,
      "[FunctionName](#cfn-lambda-eventsourcemapping-functionname)" : String,
      "[MaximumBatchingWindowInSeconds](#cfn-lambda-eventsourcemapping-maximumbatchingwindowinseconds)" : Integer,
      "[MaximumRecordAgeInSeconds](#cfn-lambda-eventsourcemapping-maximumrecordageinseconds)" : Integer,
      "[MaximumRetryAttempts](#cfn-lambda-eventsourcemapping-maximumretryattempts)" : Integer,
      "[ParallelizationFactor](#cfn-lambda-eventsourcemapping-parallelizationfactor)" : Integer,
      "[StartingPosition](#cfn-lambda-eventsourcemapping-startingposition)" : String,
      "[Topics](#cfn-lambda-eventsourcemapping-topics)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-lambda-eventsourcemapping-syntax.yaml"></a>

```
Type: AWS::Lambda::EventSourceMapping
Properties: 
  [BatchSize](#cfn-lambda-eventsourcemapping-batchsize): Integer
  [BisectBatchOnFunctionError](#cfn-lambda-eventsourcemapping-bisectbatchonfunctionerror): Boolean
  [DestinationConfig](#cfn-lambda-eventsourcemapping-destinationconfig): 
    DestinationConfig
  [Enabled](#cfn-lambda-eventsourcemapping-enabled): Boolean
  [EventSourceArn](#cfn-lambda-eventsourcemapping-eventsourcearn): String
  [FunctionName](#cfn-lambda-eventsourcemapping-functionname): String
  [MaximumBatchingWindowInSeconds](#cfn-lambda-eventsourcemapping-maximumbatchingwindowinseconds): Integer
  [MaximumRecordAgeInSeconds](#cfn-lambda-eventsourcemapping-maximumrecordageinseconds): Integer
  [MaximumRetryAttempts](#cfn-lambda-eventsourcemapping-maximumretryattempts): Integer
  [ParallelizationFactor](#cfn-lambda-eventsourcemapping-parallelizationfactor): Integer
  [StartingPosition](#cfn-lambda-eventsourcemapping-startingposition): String
  [Topics](#cfn-lambda-eventsourcemapping-topics): 
    - String
```

## Properties<a name="aws-resource-lambda-eventsourcemapping-properties"></a>

`BatchSize`  <a name="cfn-lambda-eventsourcemapping-batchsize"></a>
The maximum number of items to retrieve in a single batch\.  
+  **Amazon Kinesis** \- Default 100\. Max 10,000\.
+  **Amazon DynamoDB Streams** \- Default 100\. Max 1,000\.
+  **Amazon Simple Queue Service** \- Default 10\. Max 10\.
+  **Amazon Managed Streaming for Apache Kafka** \- Default 100\. Max 10,000\.
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BisectBatchOnFunctionError`  <a name="cfn-lambda-eventsourcemapping-bisectbatchonfunctionerror"></a>
\(Streams\) If the function returns an error, split the batch in two and retry\.  
*Required*: No  
*Type*: Boolean  
*Default*: `false`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationConfig`  <a name="cfn-lambda-eventsourcemapping-destinationconfig"></a>
\(Streams\) An Amazon SQS queue or Amazon SNS topic destination for discarded records\.  
*Required*: No  
*Type*: [DestinationConfig](aws-properties-lambda-eventsourcemapping-destinationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-lambda-eventsourcemapping-enabled"></a>
If true, the event source mapping is active\. Set to false to pause polling and invocation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventSourceArn`  <a name="cfn-lambda-eventsourcemapping-eventsourcearn"></a>
The Amazon Resource Name \(ARN\) of the event source\.  
+  **Amazon Kinesis** \- The ARN of the data stream or a stream consumer\.
+  **Amazon DynamoDB Streams** \- The ARN of the stream\.
+  **Amazon Simple Queue Service** \- The ARN of the queue\.
+  **Amazon Managed Streaming for Apache Kafka** \- The ARN of the cluster\.
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:(aws[a-zA-Z0-9-]*):([a-zA-Z0-9\-])+:([a-z]{2}(-gov)?-[a-z]+-\d{1})?:(\d{12})?:(.*)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FunctionName`  <a name="cfn-lambda-eventsourcemapping-functionname"></a>
The name of the Lambda function\.  

**Name formats**
+  **Function name** \- `MyFunction`\.
+  **Function ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:MyFunction`\.
+  **Version or Alias ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:MyFunction:PROD`\.
+  **Partial ARN** \- `123456789012:function:MyFunction`\.
The length constraint applies only to the full ARN\. If you specify only the function name, it's limited to 64 characters in length\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `(arn:(aws[a-zA-Z-]*)?:lambda:)?([a-z]{2}(-gov)?-[a-z]+-\d{1}:)?(\d{12}:)?(function:)?([a-zA-Z0-9-_]+)(:(\$LATEST|[a-zA-Z0-9-_]+))?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumBatchingWindowInSeconds`  <a name="cfn-lambda-eventsourcemapping-maximumbatchingwindowinseconds"></a>
\(Streams\) The maximum amount of time to gather records before invoking the function, in seconds\.  
*Required*: No  
*Type*: Integer  
*Default*: `0`  
*Minimum*: `0`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumRecordAgeInSeconds`  <a name="cfn-lambda-eventsourcemapping-maximumrecordageinseconds"></a>
\(Streams\) Discard records older than the specified age\. The default value is infinite \(\-1\)\. When set to infinite \(\-1\), failed records are retried until the record expires\.  
*Required*: No  
*Type*: Integer  
*Default*: `604800`  
*Minimum*: `60`  
*Maximum*: `604800`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumRetryAttempts`  <a name="cfn-lambda-eventsourcemapping-maximumretryattempts"></a>
\(Streams\) Discard records after the specified number of retries\. The default value is infinite \(\-1\)\. When set to infinite \(\-1\), failed records are retried until the record expires\.  
*Required*: No  
*Type*: Integer  
*Default*: `10000`  
*Minimum*: `0`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelizationFactor`  <a name="cfn-lambda-eventsourcemapping-parallelizationfactor"></a>
\(Streams\) The number of batches to process from each shard concurrently\.  
*Required*: No  
*Type*: Integer  
*Default*: `1`  
*Minimum*: `1`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartingPosition`  <a name="cfn-lambda-eventsourcemapping-startingposition"></a>
The position in a stream from which to start reading\. Required for Amazon Kinesis, Amazon DynamoDB, and Amazon MSK Streams sources\.  
+ **LATEST** \- Read only new records\.
+ **TRIM\_HORIZON** \- Process all available records\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Topics`  <a name="cfn-lambda-eventsourcemapping-topics"></a>
 \(MSK\) The name of the Kafka topic\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lambda-eventsourcemapping-return-values"></a>

### Ref<a name="aws-resource-lambda-eventsourcemapping-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the mapping's ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lambda-eventsourcemapping-return-values-fn--getatt"></a>

#### <a name="aws-resource-lambda-eventsourcemapping-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-lambda-eventsourcemapping--examples"></a>

### Event Source Mapping<a name="aws-resource-lambda-eventsourcemapping--examples--Event_Source_Mapping"></a>

Create an event source mapping that reads events from Amazon Kinesis and invokes a Lambda function in the same template\.

#### JSON<a name="aws-resource-lambda-eventsourcemapping--examples--Event_Source_Mapping--json"></a>

```
"EventSourceMapping": { "Type": "AWS::Lambda::EventSourceMapping", "Properties": {
        "EventSourceArn": { "Fn::Join": [ "", [ "arn:aws:kinesis:", { "Ref": "AWS::Region" }, ":", { "Ref":
        "AWS::AccountId" }, ":stream/", { "Ref": "KinesisStream" } ] ] }, "FunctionName": { "Fn::GetAtt": [
        "LambdaFunction", "Arn" ] }, "StartingPosition": "TRIM_HORIZON" } }
```

#### YAML<a name="aws-resource-lambda-eventsourcemapping--examples--Event_Source_Mapping--yaml"></a>

```
MyEventSourceMapping: Type: AWS::Lambda::EventSourceMapping Properties: EventSourceArn:
        Fn::Join: - "" - - "arn:aws:kinesis:" - Ref: "AWS::Region" - ":" - Ref: "AWS::AccountId" - ":stream/" - Ref:
        "KinesisStream" FunctionName: Fn::GetAtt: - "LambdaFunction" - "Arn" StartingPosition: "TRIM_HORIZON"
```
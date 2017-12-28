# AWS::Lambda::EventSourceMapping<a name="aws-resource-lambda-eventsourcemapping"></a>

The `AWS::Lambda::EventSourceMapping` resource specifies a stream as an event source for an AWS Lambda \(Lambda\) function\. The stream can be an Kinesis stream or an Amazon DynamoDB \(DynamoDB\) stream\. Lambda invokes the associated function when records are posted to the stream\. For more information, see [CreateEventSourceMapping](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateEventSourceMapping.html) in the *AWS Lambda Developer Guide*\.


+ [Syntax](#aws-resource-lambda-eventsourcemapping-syntax)
+ [Properties](#w3ab2c21c10d797b9)
+ [Return Values](#w3ab2c21c10d797c11)
+ [Example](#w3ab2c21c10d797c13)

## Syntax<a name="aws-resource-lambda-eventsourcemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-eventsourcemapping-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::EventSourceMapping",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-batchsize)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-enabled)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-eventsourcearn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-functionname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-startingposition)" : String
  }
}
```

### YAML<a name="aws-resource-lambda-eventsourcemapping-syntax.yaml"></a>

```
Type: "AWS::Lambda::EventSourceMapping"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-batchsize): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-enabled): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-eventsourcearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-functionname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-eventsourcemapping-startingposition): String
```

## Properties<a name="w3ab2c21c10d797b9"></a>

`BatchSize`  
The largest number of records that Lambda retrieves from your event source when invoking your function\. Your function receives an event with all the retrieved records\. For the default and valid values, see [CreateEventSourceMapping](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateEventSourceMapping.html) in the *AWS Lambda Developer Guide*\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`Enabled`  
Indicates whether Lambda begins polling the event source\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`EventSourceArn`  
The Amazon Resource Name \(ARN\) of the Kinesis or DynamoDB stream that is the source of events\. Any record added to this stream can invoke the Lambda function\. For more information, see [CreateEventSourceMapping](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateEventSourceMapping.html) in the *AWS Lambda Developer Guide*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`FunctionName`  
The name or ARN of a Lambda function to invoke when Lambda detects an event on the stream\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`StartingPosition`  
The position in the stream where Lambda starts reading\. For valid values, see [CreateEventSourceMapping](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateEventSourceMapping.html) in the *AWS Lambda Developer Guide*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d797c11"></a>

### Ref<a name="w3ab2c21c10d797c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d797c13"></a>

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
  Type: "AWS::Lambda::EventSourceMapping"
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
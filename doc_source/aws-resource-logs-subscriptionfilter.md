# AWS::Logs::SubscriptionFilter<a name="aws-resource-logs-subscriptionfilter"></a>

The `AWS::Logs::SubscriptionFilter` resource creates an Amazon CloudWatch Logs \(CloudWatch Logs\) subscription filter that defines which log events are delivered to your Kinesis stream or AWS Lambda \(Lambda\) function and where to send them\.

**Topics**
+ [Syntax](#aws-resource-logs-subscriptionfilter-syntax)
+ [Properties](#w3ab2c21c10d884b9)
+ [Return Values](#w3ab2c21c10d884c11)
+ [Example](#w3ab2c21c10d884c13)

## Syntax<a name="aws-resource-logs-subscriptionfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-subscriptionfilter-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::SubscriptionFilter",
  "Properties" : {
    "[DestinationArn](#cfn-cwl-subscriptionfilter-destinationarn)" : String,
    "[FilterPattern](#cfn-cwl-subscriptionfilter-filterpattern)" : String,
    "[LogGroupName](#cfn-cwl-subscriptionfilter-loggroupname)" : String,
    "[RoleArn](#cfn-cwl-subscriptionfilter-rolearn)" : String
  }
}
```

### YAML<a name="aws-resource-logs-subscriptionfilter-syntax.yaml"></a>

```
Type: "AWS::Logs::SubscriptionFilter"
Properties: 
  [DestinationArn](#cfn-cwl-subscriptionfilter-destinationarn): String
  [FilterPattern](#cfn-cwl-subscriptionfilter-filterpattern): String
  [LogGroupName](#cfn-cwl-subscriptionfilter-loggroupname): String
  [RoleArn](#cfn-cwl-subscriptionfilter-rolearn): String
```

## Properties<a name="w3ab2c21c10d884b9"></a>

`DestinationArn`  <a name="cfn-cwl-subscriptionfilter-destinationarn"></a>
The Amazon Resource Name \(ARN\) of the Kinesis stream, Kinesis Data Firehose delivery stream, or Lambda function that you want to use as the subscription feed destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`FilterPattern`  <a name="cfn-cwl-subscriptionfilter-filterpattern"></a>
The filtering expressions that restrict what gets delivered to the destination AWS resource\. For more information about the filter pattern syntax, see [Filter and Pattern Syntax](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/FilterAndPatternSyntax.html) in the *Amazon CloudWatch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LogGroupName`  <a name="cfn-cwl-subscriptionfilter-loggroupname"></a>
The log group to associate with the subscription filter\. All log events that are uploaded to this log group are filtered and delivered to the specified AWS resource if the filter pattern matches the log events\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RoleArn`  <a name="cfn-cwl-subscriptionfilter-rolearn"></a>
An IAM role that grants CloudWatch Logs permission to put data into the specified Kinesis stream\. For Lambda and CloudWatch Logs destinations, don't specify this property because CloudWatch Logs gets the necessary permissions from the destination resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d884c11"></a>

### Ref<a name="w3ab2c21c10d884c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d884c13"></a>

The following example sends log events that are associated with the `Root` user to an Kinesis stream\.

### JSON<a name="aws-resource-logs-subscriptionfilter-example.json"></a>

```
"SubscriptionFilter" : {
  "Type" : "AWS::Logs::SubscriptionFilter",
  "Properties" : {
    "RoleArn" : { "Fn::GetAtt" : [ "CloudWatchIAMRole", "Arn" ] },
    "LogGroupName" : { "Ref" : "LogGroup" },
    "FilterPattern" : "{$.userIdentity.type = Root}",
    "DestinationArn" : { "Fn::GetAtt" : [ "KinesisStream", "Arn" ] }
  }
}
```

### YAML<a name="aws-resource-logs-subscriptionfilter-example.yaml"></a>

```
SubscriptionFilter: 
  Type: "AWS::Logs::SubscriptionFilter"
  Properties: 
    RoleArn: 
      Fn::GetAtt: 
        - "CloudWatchIAMRole"
        - "Arn"
    LogGroupName: 
      Ref: "LogGroup"
    FilterPattern: "{$.userIdentity.type = Root}"
    DestinationArn: 
      Fn::GetAtt: 
        - "KinesisStream"
        - "Arn"
```
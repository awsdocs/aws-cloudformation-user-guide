# AWS::Logs::SubscriptionFilter<a name="aws-resource-logs-subscriptionfilter"></a>

The `AWS::Logs::SubscriptionFilter` resource specifies a subscription filter and associates it with the specified log group\. Subscription filters allow you to subscribe to a real\-time stream of log events and have them delivered to a specific destination\. Currently, the supported destinations are:
+ An Amazon Kinesis data stream belonging to the same account as the subscription filter, for same\-account delivery\.
+ A logical destination that belongs to a different account, for cross\-account delivery\.
+ An Amazon Kinesis Firehose delivery stream that belongs to the same account as the subscription filter, for same\-account delivery\.
+ An AWS Lambda function that belongs to the same account as the subscription filter, for same\-account delivery\.

There can only be one subscription filter associated with a log group\.

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
Type: AWS::Logs::SubscriptionFilter
Properties: 
  [DestinationArn](#cfn-cwl-subscriptionfilter-destinationarn): String
  [FilterPattern](#cfn-cwl-subscriptionfilter-filterpattern): String
  [LogGroupName](#cfn-cwl-subscriptionfilter-loggroupname): String
  [RoleArn](#cfn-cwl-subscriptionfilter-rolearn): String
```

## Properties<a name="aws-resource-logs-subscriptionfilter-properties"></a>

`DestinationArn`  <a name="cfn-cwl-subscriptionfilter-destinationarn"></a>
The Amazon Resource Name \(ARN\) of the destination\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FilterPattern`  <a name="cfn-cwl-subscriptionfilter-filterpattern"></a>
The filtering expressions that restrict what gets delivered to the destination AWS resource\. For more information about the filter pattern syntax, see [Filter and Pattern Syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html)\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogGroupName`  <a name="cfn-cwl-subscriptionfilter-loggroupname"></a>
The log group to associate with the subscription filter\. All log events that are uploaded to this log group are filtered and delivered to the specified AWS resource if the filter pattern matches the log events\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-cwl-subscriptionfilter-rolearn"></a>
The ARN of an IAM role that grants CloudWatch Logs permissions to deliver ingested log events to the destination stream\. You don't need to provide the ARN when you are working with a logical destination for cross\-account delivery\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-logs-subscriptionfilter-return-values"></a>

### Ref<a name="aws-resource-logs-subscriptionfilter-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-logs-subscriptionfilter--examples"></a>



### Create a Subscription Filter<a name="aws-resource-logs-subscriptionfilter--examples--Create_a_Subscription_Filter"></a>

The following example sends log events that are associated with the `Root` user to a Kinesis data stream\.

#### JSON<a name="aws-resource-logs-subscriptionfilter--examples--Create_a_Subscription_Filter--json"></a>

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

#### YAML<a name="aws-resource-logs-subscriptionfilter--examples--Create_a_Subscription_Filter--yaml"></a>

```
SubscriptionFilter: 
  Type: AWS::Logs::SubscriptionFilter
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
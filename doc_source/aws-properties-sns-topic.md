# AWS::SNS::Topic<a name="aws-properties-sns-topic"></a>

The `AWS::SNS::Topic` type creates an Amazon Simple Notification Service \(Amazon SNS\) topic\.

**Topics**
+ [Syntax](#aws-resource-sns-topic-syntax)
+ [Properties](#w3ab2c21c10e1128b9)
+ [Return Values](#w3ab2c21c10e1128c11)
+ [Examples](#w3ab2c21c10e1128c13)
+ [See Also](#w3ab2c21c10e1128c15)

## Syntax<a name="aws-resource-sns-topic-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sns-topic-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::Topic",
  "Properties" : {
    "[DisplayName](#cfn-sns-topic-displayname)" : String,
    "[Subscription](#cfn-sns-topic-subscription)" : [ SNS Subscription, ... ],
    "[TopicName](#cfn-sns-topic-name)" : String
  }
}
```

### YAML<a name="aws-resource-sns-topic-syntax.yaml"></a>

```
Type: "AWS::SNS::Topic"
Properties: 
  [DisplayName](#cfn-sns-topic-displayname): String
  [Subscription](#cfn-sns-topic-subscription):
    SNS Subscription
  [TopicName](#cfn-sns-topic-name): String
```

## Properties<a name="w3ab2c21c10e1128b9"></a>

`DisplayName`  <a name="cfn-sns-topic-displayname"></a>
A developer\-defined string that can be used to identify this SNS topic\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Subscription`  <a name="cfn-sns-topic-subscription"></a>
The SNS subscriptions \(endpoints\) for this topic\.  
*Required*: No  
*Type*: List of [SNS Subscriptions](aws-properties-sns-subscription.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TopicName`  <a name="cfn-sns-topic-name"></a>
A name for the topic\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the topic name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10e1128c11"></a>

### Ref<a name="w3ab2c21c10e1128c11b2"></a>

For the `AWS::SNS::Topic` resource, the `Ref` intrinsic function returns the topic ARN, for example: `arn:aws:sns:us-east-1:123456789012:mystack-mytopic-NZJ5JSMVGFIE`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10e1128c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`TopicName`  
Returns the name for an Amazon SNS topic\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10e1128c13"></a>

An example of an SNS topic subscribed to by two SQS queues:

### JSON<a name="aws-resource-sns-topic-example.json"></a>

```
"MySNSTopic" : {
   "Type" : "AWS::SNS::Topic",
   "Properties" : {
      "Subscription" : [
         { "Endpoint" : { "Fn::GetAtt" : [ "MyQueue1", "Arn" ] }, "Protocol" : "sqs" },
         { "Endpoint" : { "Fn::GetAtt" : [ "MyQueue2", "Arn" ] }, "Protocol" : "sqs" }
      ],
      "TopicName" : "SampleTopic"
   }
}
```

### YAML<a name="aws-resource-sns-topic-example.yaml"></a>

```
MySNSTopic: 
  Type: "AWS::SNS::Topic"
  Properties: 
    Subscription: 
      - 
        Endpoint: 
          Fn::GetAtt: 
            - "MyQueue1"
            - "Arn"
        Protocol: "sqs"
      - 
        Endpoint: 
          Fn::GetAtt: 
            - "MyQueue2"
            - "Arn"
        Protocol: "sqs"
    TopicName: "SampleTopic"
```

## See Also<a name="w3ab2c21c10e1128c15"></a>
+ [Using an AWS CloudFormation Template to Create a Topic that Sends Messages to Amazon SQS Queues](http://docs.aws.amazon.com/sns/latest/dg/SendMessageToSQS.cloudformation.html) in the *Amazon Simple Notification Service Developer Guide*
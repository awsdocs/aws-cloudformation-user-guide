# AWS::SNS::Subscription<a name="aws-resource-sns-subscription"></a>

The `AWS::SNS::Subscription` resource subscribes an endpoint to an Amazon Simple Notification Service \(Amazon SNS\) topic\. For a subscription to be created, the owner of the endpoint must confirm the subscription\.

## Syntax<a name="aws-resource-sns-subscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sns-subscription-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::Subscription",
  "Properties" : {
      "[DeliveryPolicy](#cfn-sns-subscription-deliverypolicy)" : Json,
      "[Endpoint](#cfn-sns-endpoint)" : String,
      "[FilterPolicy](#cfn-sns-subscription-filterpolicy)" : Json,
      "[Protocol](#cfn-sns-protocol)" : String,
      "[RawMessageDelivery](#cfn-sns-subscription-rawmessagedelivery)" : Boolean,
      "[RedrivePolicy](#cfn-sns-subscription-redrivepolicy)" : Json,
      "[Region](#cfn-sns-subscription-region)" : String,
      "[SubscriptionRoleArn](#cfn-sns-subscription-subscriptionrolearn)" : String,
      "[TopicArn](#topicarn)" : String
    }
}
```

### YAML<a name="aws-resource-sns-subscription-syntax.yaml"></a>

```
Type: AWS::SNS::Subscription
Properties: 
  [DeliveryPolicy](#cfn-sns-subscription-deliverypolicy): Json
  [Endpoint](#cfn-sns-endpoint): String
  [FilterPolicy](#cfn-sns-subscription-filterpolicy): Json
  [Protocol](#cfn-sns-protocol): String
  [RawMessageDelivery](#cfn-sns-subscription-rawmessagedelivery): Boolean
  [RedrivePolicy](#cfn-sns-subscription-redrivepolicy): Json
  [Region](#cfn-sns-subscription-region): String
  [SubscriptionRoleArn](#cfn-sns-subscription-subscriptionrolearn): String
  [TopicArn](#topicarn): String
```

## Properties<a name="aws-resource-sns-subscription-properties"></a>

`DeliveryPolicy`  <a name="cfn-sns-subscription-deliverypolicy"></a>
The delivery policy JSON assigned to the subscription\. Enables the subscriber to define the message delivery retry strategy in the case of an HTTP/S endpoint subscribed to the topic\. For more information, see ` [GetSubscriptionAttributes](https://docs.aws.amazon.com/sns/latest/api/API_GetSubscriptionAttributes.html) ` in the *Amazon Simple Notification Service API Reference* and [Message Delivery Retries](https://docs.aws.amazon.com/sns/latest/dg/sns-message-delivery-retries.html) in the *Amazon SNS Developer Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-sns-endpoint"></a>
The subscription's endpoint\. The endpoint value depends on the protocol that you specify\. For more information, see the `Endpoint` parameter of the ` [Subscribe](https://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) ` action in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FilterPolicy`  <a name="cfn-sns-subscription-filterpolicy"></a>
The filter policy JSON assigned to the subscription\. Enables the subscriber to filter out unwanted messages\. For more information, see ` [GetSubscriptionAttributes](https://docs.aws.amazon.com/sns/latest/api/API_GetSubscriptionAttributes.html) ` in the *Amazon Simple Notification Service API Reference* and [Message Filtering](https://docs.aws.amazon.com/sns/latest/dg/sns-message-filtering.html) in the *Amazon SNS Developer Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-sns-protocol"></a>
The subscription's protocol\. For more information, see the `Protocol` parameter of the ` [Subscribe](https://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) ` action in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RawMessageDelivery`  <a name="cfn-sns-subscription-rawmessagedelivery"></a>
When set to `true`, enables raw message delivery\. Raw messages don't contain any JSON formatting and can be sent to Amazon SQS and HTTP/S endpoints\. For more information, see ` [GetSubscriptionAttributes](https://docs.aws.amazon.com/sns/latest/api/API_GetSubscriptionAttributes.html) ` in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedrivePolicy`  <a name="cfn-sns-subscription-redrivepolicy"></a>
When specified, sends undeliverable messages to the specified Amazon SQS dead\-letter queue\. Messages that can't be delivered due to client errors \(for example, when the subscribed endpoint is unreachable\) or server errors \(for example, when the service that powers the subscribed endpoint becomes unavailable\) are held in the dead\-letter queue for further analysis or reprocessing\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-sns-subscription-region"></a>
For cross\-region subscriptions, the region in which the topic resides\.  
If no region is specified, CloudFormation uses the region of the caller as the default\.  
If you perform an update operation that only updates the `Region` property of a `AWS::SNS::Subscription` resource, that operation will fail unless you are either:  
+ Updating the `Region` from `NULL` to the caller region\.
+ Updating the `Region` from the caller region to `NULL`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubscriptionRoleArn`  <a name="cfn-sns-subscription-subscriptionrolearn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="topicarn"></a>
The ARN of the topic to subscribe to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-sns-subscription--examples"></a>



### Create a subscription with mandatory attributes<a name="aws-resource-sns-subscription--examples--Create_a_subscription_with_mandatory_attributes"></a>

The following example creates a subscription with only an endpoint, protocol, and topic ARN\.

#### JSON<a name="aws-resource-sns-subscription--examples--Create_a_subscription_with_mandatory_attributes--json"></a>

```
"MySubscription" : {
  "Type" : "AWS::SNS::Subscription",
  "Properties" : {
    "Endpoint" : "test@example.com",
    "Protocol" : "email",
    "TopicArn" : { "Ref" : "MySNSTopic" }
  }
}
```

#### YAML<a name="aws-resource-sns-subscription--examples--Create_a_subscription_with_mandatory_attributes--yaml"></a>

```
MySubscription:
  Type: AWS::SNS::Subscription
  Properties:
    Endpoint: test@example.com
    Protocol: email
    TopicArn: !Ref 'MySNSTopic'
```

### Create a subscription with optional attributes<a name="aws-resource-sns-subscription--examples--Create_a_subscription_with_optional_attributes"></a>

The following example creates a subscription with a filter policy, delivery policy, and raw message delivery enabled\.

**Note**  
You can set subscription attributes only on standalone Amazon SNS subscriptions \(not on subscriptions nested in topics\)\.

#### YAML<a name="aws-resource-sns-subscription--examples--Create_a_subscription_with_optional_attributes--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  CarSalesTopic:
    Type: 'AWS::SNS::Topic'
  ERPSubscription:
    Type: 'AWS::SNS::Subscription'
    Properties:
      TopicArn: !Ref CarSalesTopic
      Endpoint: !GetAtt 
        - ERPIntegrationQueue
        - Arn
      Protocol: sqs
      RawMessageDelivery: 'true'
  CRMSubscription:
    Type: 'AWS::SNS::Subscription'
    Properties:
      TopicArn: !Ref CarSalesTopic
      Endpoint: !GetAtt 
        - CRMIntegrationQueue
        - Arn
      Protocol: sqs
      RawMessageDelivery: 'true'
      FilterPolicy:
        buyer-class:
          - vip
  SCMSubscription:
    Type: 'AWS::SNS::Subscription'
    Properties:
      TopicArn: !Ref CarSalesTopic
      Endpoint: !Ref myHttpEndpoint
      Protocol: https
      DeliveryPolicy:
        healthyRetryPolicy:
          numRetries: 20
          minDelayTarget: 10
          maxDelayTarget: 30
          numMinDelayRetries: 3
          numMaxDelayRetries: 17
          numNoDelayRetries: 0
          backoffFunction: exponential
  ERPIntegrationQueue:
    Type: 'AWS::SQS::Queue'
    Properties: {}
  CRMIntegrationQueue:
    Type: 'AWS::SQS::Queue'
    Properties: {}
Parameters:
  myHttpEndpoint:
    Type: String
```

#### JSON<a name="aws-resource-sns-subscription--examples--Create_a_subscription_with_optional_attributes--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "CarSalesTopic": {
            "Type": "AWS::SNS::Topic"
        },
        "ERPSubscription": {
            "Type": "AWS::SNS::Subscription",
            "Properties": {
                "TopicArn": {
                    "Ref": "CarSalesTopic"
                },
                "Endpoint": {
                    "Fn::GetAtt": ["ERPIntegrationQueue", "Arn"]
                },
                "Protocol": "sqs",
                "RawMessageDelivery": "true"
            }
        },
        "CRMSubscription": {
            "Type": "AWS::SNS::Subscription",
            "Properties": {
                "TopicArn": {
                    "Ref": "CarSalesTopic"
                },
                "Endpoint": {
                    "Fn::GetAtt": ["CRMIntegrationQueue", "Arn"]
                },
                "Protocol": "sqs",
                "RawMessageDelivery": "true",
                "FilterPolicy": {
                    "buyer-class": [
                        "vip"
                    ]
                }
            }
        },
        "SCMSubscription": {
            "Type": "AWS::SNS::Subscription",
            "Properties": {
                "TopicArn": {
                    "Ref": "CarSalesTopic"
                },
                "Endpoint": {
                    "Ref": "myHttpEndpoint"
                },
                "Protocol": "https",
                "DeliveryPolicy": {
                    "healthyRetryPolicy": {
                        "numRetries": 20,
                        "minDelayTarget": 10,
                        "maxDelayTarget": 30,
                        "numMinDelayRetries": 3,
                        "numMaxDelayRetries": 17,
                        "numNoDelayRetries": 0,
                        "backoffFunction": "exponential"
                    }
                }
            }
        },
        "ERPIntegrationQueue": {
            "Type": "AWS::SQS::Queue",
            "Properties": {}
        },
        "CRMIntegrationQueue": {
            "Type": "AWS::SQS::Queue",
            "Properties": {}
        }
    },
    "Parameters": {
        "myHttpEndpoint": {
            "Type": "String"
        }
    }
}
```
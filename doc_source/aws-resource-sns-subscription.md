# AWS::SNS::Subscription<a name="aws-resource-sns-subscription"></a>

The `AWS::SNS::Subscription` resource subscribes an endpoint to an Amazon Simple Notification Service \(Amazon SNS\) topic\. The owner of the endpoint must confirm the subscription before Amazon SNS creates the subscription\.

## Syntax<a name="aws-resource-sns-subscription-syntax"></a>

### JSON<a name="aws-resource-sns-subscription-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::Subscription",
  "Properties" : {
    "[DeliveryPolicy](#cfn-sns-subscription-deliverypolicy)" : JSON object,
    "[Endpoint](#cfn-sns-endpoint)" : String,
    "[FilterPolicy](#cfn-sns-subscription-filterpolicy)" : JSON object,
    "[Protocol](#cfn-sns-protocol)" : String,
    "[RawMessageDelivery](#cfn-sns-subscription-rawmessagedelivery)" : Boolean,
    "[Region](#cfn-sns-subscription-region)" : String,
    "[TopicArn](#cfn-sns-topicarn)" : String
  }
}
```

### YAML<a name="aws-resource-sns-subscription-syntax.yaml"></a>

```
Type: "AWS::SNS::Subscription"
Properties:
  [DeliveryPolicy](#cfn-sns-subscription-deliverypolicy): JSON object
  [Endpoint](#cfn-sns-endpoint): String
  [FilterPolicy](#cfn-sns-subscription-filterpolicy): JSON object
  [Protocol](#cfn-sns-protocol): String
  [RawMessageDelivery](#cfn-sns-subscription-rawmessagedelivery): Boolean,
  [Region](#cfn-sns-subscription-region): String
  [TopicArn](#cfn-sns-topicarn): String
```

## Properties<a name="aws-resource-sns-subscription-properties"></a>

`DeliveryPolicy`  <a name="cfn-sns-subscription-deliverypolicy"></a>
The JSON serialization of the subscription's delivery policy\. For more information, see [GetSubscriptionAttributes](https://docs.aws.amazon.com/sns/latest/api/API_GetSubscriptionAttributes.html) in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Endpoint`  <a name="cfn-sns-endpoint"></a>
The endpoint that receives notifications from the Amazon SNS topic\. The endpoint value depends on the protocol that you specify\. For more information, see the [Subscribe Endpoint](https://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`FilterPolicy`  <a name="cfn-sns-subscription-filterpolicy"></a>
The filter policy JSON that is assigned to the subscription\. For more information, see [GetSubscriptionAttributes](https://docs.aws.amazon.com/sns/latest/api/API_GetSubscriptionAttributes.html) in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Protocol`  <a name="cfn-sns-protocol"></a>
The subscription's protocol\. For more information, see the [Subscribe Protocol](https://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RawMessageDelivery`  <a name="cfn-sns-subscription-rawmessagedelivery"></a>
`true` if raw message delivery is enabled for the subscription\. Raw messages are free of JSON formatting and can be sent to HTTP/S and Amazon SQS endpoints\. For more information, see [GetSubscriptionAttributes](https://docs.aws.amazon.com/sns/latest/api/API_GetSubscriptionAttributes.html) in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Region`  <a name="cfn-sns-subscription-region"></a>
For cross\-region subscriptions, the region in which the topic resides\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TopicArn`  <a name="cfn-sns-topicarn"></a>
The Amazon Resource Name \(ARN\) of the topic to subscribe to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Example<a name="aws-resource-sns-subscription-examples"></a>

### Create a subscription with mandatory attributes<a name="aws-resource-sns-subscription-example1"></a>

The following example creates a subscription with Endpoint, Protocol and TopicArn only\.

#### JSON<a name="aws-resource-sns-subscription-example1.json"></a>

```
"MySubscription" : {
  "Type" : "AWS::SNS::Subscription",
  "Properties" : {
    "Endpoint" : "test@email.com",
    "Protocol" : "email",
    "TopicArn" : {"Ref" : "MySNSTopic"}
  }
}
```

#### YAML<a name="aws-resource-sns-subscription-example1.yaml"></a>

```
MySubscription:
  Type: AWS::SNS::Subscription
  Properties:
    Endpoint: test@email.com
    Protocol: email
    TopicArn: !Ref 'MySNSTopic'
```

### Create a subscription with optional attributes<a name="aws-resource-sns-subscription-example2"></a>

The following example creates a subscription with FilterPolicy, DeliveryPolicy and RawMessageDelivery\.

Note that SNS subscription attributes can be set on standalone SNS subscriptions only, as opposed to SNS subscriptions nested in SNS topics\.

#### JSON<a name="aws-resource-sns-subscription-example2.json"></a>

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

#### YAML<a name="aws-resource-sns-subscription-example2.yaml"></a>

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
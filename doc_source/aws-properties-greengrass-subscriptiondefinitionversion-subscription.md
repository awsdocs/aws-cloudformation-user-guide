# AWS::Greengrass::SubscriptionDefinitionVersion Subscription<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription"></a>

<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription-description"></a>Subscriptions define how MQTT messages can be exchanged between devices, functions, and connectors in the group, and with AWS IoT or the local shadow service\. A subscription defines a message source, message target, and a topic \(or subject\) that's used to route messages from the source to the target\. A subscription defines the message flow in one direction, from the source to the target\. For two\-way communication, you must set up two subscriptions, one for each direction\.

<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription-inheritance"></a> In an AWS CloudFormation template, the `Subscriptions` property of the [ `AWS::Greengrass::SubscriptionDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinitionversion.html) resource contains a list of `Subscription` property types\.

## Syntax<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription-syntax.json"></a>

```
{
  "[Id](#cfn-greengrass-subscriptiondefinitionversion-subscription-id)" : String,
  "[Source](#cfn-greengrass-subscriptiondefinitionversion-subscription-source)" : String,
  "[Subject](#cfn-greengrass-subscriptiondefinitionversion-subscription-subject)" : String,
  "[Target](#cfn-greengrass-subscriptiondefinitionversion-subscription-target)" : String
}
```

### YAML<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription-syntax.yaml"></a>

```
  [Id](#cfn-greengrass-subscriptiondefinitionversion-subscription-id): String
  [Source](#cfn-greengrass-subscriptiondefinitionversion-subscription-source): String
  [Subject](#cfn-greengrass-subscriptiondefinitionversion-subscription-subject): String
  [Target](#cfn-greengrass-subscriptiondefinitionversion-subscription-target): String
```

## Properties<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription-properties"></a>

`Id`  <a name="cfn-greengrass-subscriptiondefinitionversion-subscription-id"></a>
A descriptive or arbitrary ID for the subscription\. This value must be unique within the subscription definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Source`  <a name="cfn-greengrass-subscriptiondefinitionversion-subscription-source"></a>
The originator of the message\. The value can be a thing ARN, the ARN of a Lambda function alias \(recommended\) or version, a connector ARN, `cloud` \(which represents the AWS IoT cloud\), or `GGShadowService`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subject`  <a name="cfn-greengrass-subscriptiondefinitionversion-subscription-subject"></a>
The MQTT topic used to route the message\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Target`  <a name="cfn-greengrass-subscriptiondefinitionversion-subscription-target"></a>
The destination of the message\. The value can be a thing ARN, the ARN of a Lambda function alias \(recommended\) or version, a connector ARN, `cloud` \(which represents the AWS IoT cloud\), or `GGShadowService`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-subscriptiondefinitionversion-subscription--seealso"></a>
+  [Subscription](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-subscription.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 
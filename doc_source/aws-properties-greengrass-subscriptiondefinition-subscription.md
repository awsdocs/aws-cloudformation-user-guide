# AWS IoT Greengrass SubscriptionDefinition Subscription<a name="aws-properties-greengrass-subscriptiondefinition-subscription"></a>

<a name="aws-properties-greengrass-subscriptiondefinition-subscription-description"></a>Subscriptions define how MQTT messages can be exchanged between devices, functions, and connectors in the group, and with AWS IoT or the local shadow service\. A subscription defines a message source, message target, and a topic \(or subject\) that's used to route messages from the source to the target\. A subscription defines the message flow in one direction, from the source to the target\. For two\-way communication, you must set up two subscriptions, one for each direction\. 

<a name="aws-properties-greengrass-subscriptiondefinition-subscription-inheritance"></a> In an AWS CloudFormation template, the `Subscriptions` property of the [AWS IoT Greengrass SubscriptionDefinition SubscriptionDefinitionVersion](aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion.md) property type contains a list of `Subscription` property types\.

## Syntax<a name="aws-properties-greengrass-subscriptiondefinition-subscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-subscriptiondefinition-subscription-syntax.json"></a>

```
{
  "[Target](#cfn-greengrass-subscriptiondefinition-subscription-target)" : String,
  "[Id](#cfn-greengrass-subscriptiondefinition-subscription-id)" : String,
  "[Source](#cfn-greengrass-subscriptiondefinition-subscription-source)" : String,
  "[Subject](#cfn-greengrass-subscriptiondefinition-subscription-subject)" : String
}
```

### YAML<a name="aws-properties-greengrass-subscriptiondefinition-subscription-syntax.yaml"></a>

```
[Target](#cfn-greengrass-subscriptiondefinition-subscription-target): String
[Id](#cfn-greengrass-subscriptiondefinition-subscription-id): String
[Source](#cfn-greengrass-subscriptiondefinition-subscription-source): String
[Subject](#cfn-greengrass-subscriptiondefinition-subscription-subject): String
```

## Properties<a name="aws-properties-greengrass-subscriptiondefinition-subscription-properties"></a>

`Target`  <a name="cfn-greengrass-subscriptiondefinition-subscription-target"></a>
The destination of the message\. The value can be a thing ARN, a Lambda function ARN, a connector ARN, `cloud` \(which represents the AWS IoT cloud\), or `GGShadowService`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Id`  <a name="cfn-greengrass-subscriptiondefinition-subscription-id"></a>
A descriptive or arbitrary ID for the subscription\. This value must be unique within the subscription definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Source`  <a name="cfn-greengrass-subscriptiondefinition-subscription-source"></a>
The originator of the message\. The value can be a thing ARN, a Lambda function ARN, a connector ARN, `cloud` \(which represents the AWS IoT cloud\), or `GGShadowService`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Subject`  <a name="cfn-greengrass-subscriptiondefinition-subscription-subject"></a>
The MQTT topic used to route the message\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-subscriptiondefinition-subscription-seealso"></a>
+ [Subscription](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-subscription.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)
# AWS::Greengrass::SubscriptionDefinition SubscriptionDefinitionVersion<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion"></a>

<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-description"></a> A subscription definition version contains a list of [subscriptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-subscriptiondefinition-subscription.html)\.

**Note**  
After you create a subscription definition version that contains the subscriptions you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-inheritance"></a> In an AWS CloudFormation template, `SubscriptionDefinitionVersion` is the property type of the `InitialVersion` property in the [ `AWS::Greengrass::SubscriptionDefinition` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html) resource\.

## Syntax<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-syntax.json"></a>

```
{
  "[Subscriptions](#cfn-greengrass-subscriptiondefinition-subscriptiondefinitionversion-subscriptions)" : [ Subscription, ... ]
}
```

### YAML<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-syntax.yaml"></a>

```
  [Subscriptions](#cfn-greengrass-subscriptiondefinition-subscriptiondefinitionversion-subscriptions): 
    - Subscription
```

## Properties<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-properties"></a>

`Subscriptions`  <a name="cfn-greengrass-subscriptiondefinition-subscriptiondefinitionversion-subscriptions"></a>
The subscriptions in this version\.  
*Required*: Yes  
*Type*: List of [Subscription](aws-properties-greengrass-subscriptiondefinition-subscription.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion--seealso"></a>
+  [SubscriptionDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-subscriptiondefinitionversion.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 
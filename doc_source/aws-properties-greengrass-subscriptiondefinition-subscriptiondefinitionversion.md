# AWS IoT Greengrass SubscriptionDefinition SubscriptionDefinitionVersion<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion"></a>

<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-description"></a> A subscription definition version contains a list of [subscriptions](aws-properties-greengrass-subscriptiondefinition-subscription.md)\.

**Note**  
After you create a subscription definition version that contains the subscriptions you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-inheritance"></a> In an AWS CloudFormation template, `SubscriptionDefinitionVersion` is the property type of the `InitialVersion` property in the [AWS::Greengrass::SubscriptionDefinition](aws-resource-greengrass-subscriptiondefinition.md) resource\.

## Syntax<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-syntax.json"></a>

```
{
  "[Subscriptions](#cfn-greengrass-subscriptiondefinition-subscriptiondefinitionversion-subscriptions)" : [ [*Subscription*](aws-properties-greengrass-subscriptiondefinition-subscription.md), ... ]
}
```

### YAML<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-syntax.yaml"></a>

```
[Subscriptions](#cfn-greengrass-subscriptiondefinition-subscriptiondefinitionversion-subscriptions): 
  - [*Subscription*](aws-properties-greengrass-subscriptiondefinition-subscription.md)
```

## Properties<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-properties"></a>

`Subscriptions`  <a name="cfn-greengrass-subscriptiondefinition-subscriptiondefinitionversion-subscriptions"></a>
The subscriptions in this version\.  
 *Required*: Yes  
 *Type*: List of [Subscription](aws-properties-greengrass-subscriptiondefinition-subscription.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion-seealso"></a>
+ [SubscriptionDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-subscriptiondefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)
# AWS IoT Greengrass Group GroupVersion<a name="aws-properties-greengrass-group-groupversion"></a>

<a name="aws-properties-greengrass-group-groupversion-description"></a>A group version in AWS IoT Greengrass, which references of a core definition version, device definition version, subscription definition version, and other version types that contain the components you want to deploy to a Greengrass core device\. The group version must reference a core definition version that contains one core\. Other version types are optionally included, depending on your business need\.

<a name="aws-properties-greengrass-group-groupversion-inheritance"></a> In an AWS CloudFormation template, `GroupVersion` is the property type of the `InitialVersion` property in the [AWS::Greengrass::Group](aws-resource-greengrass-group.md) resource\.

## Syntax<a name="aws-properties-greengrass-group-groupversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-group-groupversion-syntax.json"></a>

```
{
  "[LoggerDefinitionVersionArn](#cfn-greengrass-group-groupversion-loggerdefinitionversionarn)" : String,
  "[DeviceDefinitionVersionArn](#cfn-greengrass-group-groupversion-devicedefinitionversionarn)" : String,
  "[FunctionDefinitionVersionArn](#cfn-greengrass-group-groupversion-functiondefinitionversionarn)" : String,
  "[CoreDefinitionVersionArn](#cfn-greengrass-group-groupversion-coredefinitionversionarn)" : String,
  "[ResourceDefinitionVersionArn](#cfn-greengrass-group-groupversion-resourcedefinitionversionarn)" : String,
  "[ConnectorDefinitionVersionArn](#cfn-greengrass-group-groupversion-connectordefinitionversionarn)" : String,
  "[SubscriptionDefinitionVersionArn](#cfn-greengrass-group-groupversion-subscriptiondefinitionversionarn)" : String
}
```

### YAML<a name="aws-properties-greengrass-group-groupversion-syntax.yaml"></a>

```
[LoggerDefinitionVersionArn](#cfn-greengrass-group-groupversion-loggerdefinitionversionarn): String
[DeviceDefinitionVersionArn](#cfn-greengrass-group-groupversion-devicedefinitionversionarn): String
[FunctionDefinitionVersionArn](#cfn-greengrass-group-groupversion-functiondefinitionversionarn): String
[CoreDefinitionVersionArn](#cfn-greengrass-group-groupversion-coredefinitionversionarn): String
[ResourceDefinitionVersionArn](#cfn-greengrass-group-groupversion-resourcedefinitionversionarn): String
[ConnectorDefinitionVersionArn](#cfn-greengrass-group-groupversion-connectordefinitionversionarn): String
[SubscriptionDefinitionVersionArn](#cfn-greengrass-group-groupversion-subscriptiondefinitionversionarn): String
```

## Properties<a name="aws-properties-greengrass-group-groupversion-properties"></a>

`LoggerDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-loggerdefinitionversionarn"></a>
The Amazon Resource Name \(ARN\) of the logger definition version that contains the loggers you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DeviceDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-devicedefinitionversionarn"></a>
The ARN of the device definition version that contains the devices you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`FunctionDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-functiondefinitionversionarn"></a>
The ARN of the function definition version that contains the functions you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CoreDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-coredefinitionversionarn"></a>
The ARN of the core definition version that contains the core you want to deploy with the group version\. Currently, the core definition version can contain only one core\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourceDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-resourcedefinitionversionarn"></a>
The ARN of the resource definition version that contains the resources you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ConnectorDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-connectordefinitionversionarn"></a>
The ARN of the connector definition version that contains the connectors you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SubscriptionDefinitionVersionArn`  <a name="cfn-greengrass-group-groupversion-subscriptiondefinitionversionarn"></a>
The ARN of the subscription definition version that contains the subscriptions you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-group-groupversion-seealso"></a>
+ [CreateGroupVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/creategroupversion-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)
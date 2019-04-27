# AWS::Greengrass::GroupVersion<a name="aws-resource-greengrass-groupversion"></a>

The `AWS::Greengrass::GroupVersion` resource represents a group version in AWS IoT Greengrass\. A group version references a core definition version, device definition version, subscription definition version, and other version types that contain the components you want to deploy to a Greengrass core device\. The group version must reference a core definition version that contains one core\. Other version types are optionally included, depending on your business need\.

**Note**  
To create a group version, you must specify the ID of the group that you want to associate with the version\. For information about creating a group, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-groupversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-groupversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::GroupVersion",
  "Properties" : {
    "[LoggerDefinitionVersionArn](#cfn-greengrass-groupversion-loggerdefinitionversionarn)" : String,
    "[DeviceDefinitionVersionArn](#cfn-greengrass-groupversion-devicedefinitionversionarn)" : String,
    "[FunctionDefinitionVersionArn](#cfn-greengrass-groupversion-functiondefinitionversionarn)" : String,
    "[CoreDefinitionVersionArn](#cfn-greengrass-groupversion-coredefinitionversionarn)" : String,
    "[ResourceDefinitionVersionArn](#cfn-greengrass-groupversion-resourcedefinitionversionarn)" : String,
    "[ConnectorDefinitionVersionArn](#cfn-greengrass-groupversion-connectordefinitionversionarn)" : String,
    "[SubscriptionDefinitionVersionArn](#cfn-greengrass-groupversion-subscriptiondefinitionversionarn)" : String,
    "[GroupId](#cfn-greengrass-groupversion-groupid)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-groupversion-syntax.yaml"></a>

```
Type: "AWS::Greengrass::GroupVersion"
Properties:
  [LoggerDefinitionVersionArn](#cfn-greengrass-groupversion-loggerdefinitionversionarn): String
  [DeviceDefinitionVersionArn](#cfn-greengrass-groupversion-devicedefinitionversionarn): String
  [FunctionDefinitionVersionArn](#cfn-greengrass-groupversion-functiondefinitionversionarn): String
  [CoreDefinitionVersionArn](#cfn-greengrass-groupversion-coredefinitionversionarn): String
  [ResourceDefinitionVersionArn](#cfn-greengrass-groupversion-resourcedefinitionversionarn): String
  [ConnectorDefinitionVersionArn](#cfn-greengrass-groupversion-connectordefinitionversionarn): String
  [SubscriptionDefinitionVersionArn](#cfn-greengrass-groupversion-subscriptiondefinitionversionarn): String
  [GroupId](#cfn-greengrass-groupversion-groupid): String
```

## Properties<a name="aws-resource-greengrass-groupversion-properties"></a>

`LoggerDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-loggerdefinitionversionarn"></a>
The Amazon Resource Name \(ARN\) of the logger definition version that contains the loggers you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DeviceDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-devicedefinitionversionarn"></a>
The ARN of the device definition version that contains the devices you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`FunctionDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-functiondefinitionversionarn"></a>
The ARN of the function definition version that contains the functions you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CoreDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-coredefinitionversionarn"></a>
The ARN of the core definition version that contains the core you want to deploy with the group version\. Currently, the core definition version can contain only one core\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourceDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-resourcedefinitionversionarn"></a>
The ARN of the resource definition version that contains the resources you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ConnectorDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-connectordefinitionversionarn"></a>
The ARN of the connector definition version that contains the connectors you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SubscriptionDefinitionVersionArn`  <a name="cfn-greengrass-groupversion-subscriptiondefinitionversionarn"></a>
The ARN of the subscription definition version that contains the subscriptions you want to deploy with the group version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`GroupId`  <a name="cfn-greengrass-groupversion-groupid"></a>
The ID of the group associated with this version\. This value is a GUID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-greengrass-groupversion-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-groupversion-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::GroupVersion` resource to the intrinsic `Ref` function, the function returns the ARN of the group version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/groups/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## See Also<a name="aws-resource-greengrass-groupversion-seealso"></a>
+ [CreateGroupVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/creategroupversion-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)
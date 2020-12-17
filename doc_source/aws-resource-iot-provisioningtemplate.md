# AWS::IoT::ProvisioningTemplate<a name="aws-resource-iot-provisioningtemplate"></a>

Creates a fleet provisioning template\.

## Syntax<a name="aws-resource-iot-provisioningtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-provisioningtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::ProvisioningTemplate",
  "Properties" : {
      "[Description](#cfn-iot-provisioningtemplate-description)" : String,
      "[Enabled](#cfn-iot-provisioningtemplate-enabled)" : Boolean,
      "[PreProvisioningHook](#cfn-iot-provisioningtemplate-preprovisioninghook)" : ProvisioningHook,
      "[ProvisioningRoleArn](#cfn-iot-provisioningtemplate-provisioningrolearn)" : String,
      "[Tags](#cfn-iot-provisioningtemplate-tags)" : Tags,
      "[TemplateBody](#cfn-iot-provisioningtemplate-templatebody)" : String,
      "[TemplateName](#cfn-iot-provisioningtemplate-templatename)" : String
    }
}
```

### YAML<a name="aws-resource-iot-provisioningtemplate-syntax.yaml"></a>

```
Type: AWS::IoT::ProvisioningTemplate
Properties: 
  [Description](#cfn-iot-provisioningtemplate-description): String
  [Enabled](#cfn-iot-provisioningtemplate-enabled): Boolean
  [PreProvisioningHook](#cfn-iot-provisioningtemplate-preprovisioninghook): 
    ProvisioningHook
  [ProvisioningRoleArn](#cfn-iot-provisioningtemplate-provisioningrolearn): String
  [Tags](#cfn-iot-provisioningtemplate-tags): 
    Tags
  [TemplateBody](#cfn-iot-provisioningtemplate-templatebody): String
  [TemplateName](#cfn-iot-provisioningtemplate-templatename): String
```

## Properties<a name="aws-resource-iot-provisioningtemplate-properties"></a>

`Description`  <a name="cfn-iot-provisioningtemplate-description"></a>
The description of the fleet provisioning template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-iot-provisioningtemplate-enabled"></a>
True to enable the fleet provisioning template, otherwise false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreProvisioningHook`  <a name="cfn-iot-provisioningtemplate-preprovisioninghook"></a>
Creates a pre\-provisioning hook template\.  
*Required*: No  
*Type*: [ProvisioningHook](aws-properties-iot-provisioningtemplate-provisioninghook.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisioningRoleArn`  <a name="cfn-iot-provisioningtemplate-provisioningrolearn"></a>
The role ARN for the role associated with the fleet provisioning template\. This IoT role grants permission to provision a device\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-provisioningtemplate-tags"></a>
Metadata which can be used to manage the fleet provisioning template\.  
*Required*: No  
*Type*: [Tags](aws-properties-iot-provisioningtemplate-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateBody`  <a name="cfn-iot-provisioningtemplate-templatebody"></a>
The name of the fleet provisioning template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-iot-provisioningtemplate-templatename"></a>
The name of the fleet provisioning template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-provisioningtemplate-return-values"></a>

### Ref<a name="aws-resource-iot-provisioningtemplate-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the thing name\. For example:

 `{ "Ref": "MyTemplate" }` 

For a stack named MyStack, a value similar to the following is returned:

 `MyStack-MyTemplate-AB1CDEFGHIJK` 

### Fn::GetAtt<a name="aws-resource-iot-provisioningtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-provisioningtemplate-return-values-fn--getatt-fn--getatt"></a>

`TemplateArn`  <a name="TemplateArn-fn::getatt"></a>
The ARN that identifies the provisioning template\.
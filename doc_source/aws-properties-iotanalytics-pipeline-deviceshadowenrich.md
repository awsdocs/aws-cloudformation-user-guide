# AWS IoT Analytics Pipeline DeviceShadowEnrich<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich"></a>

<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-description"></a>The `DeviceShadowEnrich` property type specifies information from the AWS IoT Device Shadows service to add to a message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-inheritance"></a> `DeviceShadowEnrich` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-syntax.json"></a>

```
{
  "[Attribute](#cfn-iotanalytics-pipeline-deviceshadowenrich-attribute)" : String,
  "[Name](#cfn-iotanalytics-pipeline-deviceshadowenrich-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-deviceshadowenrich-next)" : String,
  "[RoleArn](#cfn-iotanalytics-pipeline-deviceshadowenrich-rolearn)" : String,
  "[ThingName](#cfn-iotanalytics-pipeline-deviceshadowenrich-thingname)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-syntax.yaml"></a>

```
[Attribute](#cfn-iotanalytics-pipeline-deviceshadowenrich-attribute): String
[Name](#cfn-iotanalytics-pipeline-deviceshadowenrich-name): String
[Next](#cfn-iotanalytics-pipeline-deviceshadowenrich-next): String
[RoleArn](#cfn-iotanalytics-pipeline-deviceshadowenrich-rolearn): String
[ThingName](#cfn-iotanalytics-pipeline-deviceshadowenrich-thingname): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-properties"></a>

`Attribute`  <a name="cfn-iotanalytics-pipeline-deviceshadowenrich-attribute"></a>
The name of the attribute that is added to the message\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-deviceshadowenrich-name"></a>
The name of the 'deviceShadowEnrich' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-deviceshadowenrich-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-iotanalytics-pipeline-deviceshadowenrich-rolearn"></a>
The ARN of the role that allows access to the device's shadow\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ThingName`  <a name="cfn-iotanalytics-pipeline-deviceshadowenrich-thingname"></a>
The name of the IoT device whose shadow information is added to the message\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-deviceshadowenrich-seealso"></a>
+ [ CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *AWS IoT Analytics User Guide*
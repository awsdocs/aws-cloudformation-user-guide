# AWS IoT Analytics Pipeline DeviceRegistryEnrich<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich"></a>

<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-description"></a>The `DeviceRegistryEnrich` property type specifies data from the AWS IoT device registry which you can add to your message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-inheritance"></a> `DeviceRegistryEnrich` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-syntax.json"></a>

```
{
  "[Attribute](#cfn-iotanalytics-pipeline-deviceregistryenrich-attribute)" : String,
  "[Name](#cfn-iotanalytics-pipeline-deviceregistryenrich-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-deviceregistryenrich-next)" : String,
  "[RoleArn](#cfn-iotanalytics-pipeline-deviceregistryenrich-rolearn)" : String,
  "[ThingName](#cfn-iotanalytics-pipeline-deviceregistryenrich-thingname)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-syntax.yaml"></a>

```
[Attribute](#cfn-iotanalytics-pipeline-deviceregistryenrich-attribute): String
[Name](#cfn-iotanalytics-pipeline-deviceregistryenrich-name): String
[Next](#cfn-iotanalytics-pipeline-deviceregistryenrich-next): String
[RoleArn](#cfn-iotanalytics-pipeline-deviceregistryenrich-rolearn): String
[ThingName](#cfn-iotanalytics-pipeline-deviceregistryenrich-thingname): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-properties"></a>

`Attribute`  <a name="cfn-iotanalytics-pipeline-deviceregistryenrich-attribute"></a>
The name of the attribute that is added to the message\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-deviceregistryenrich-name"></a>
The name of the "deviceRegistryEnrich" activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-deviceregistryenrich-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-iotanalytics-pipeline-deviceregistryenrich-rolearn"></a>
The ARN of the role that allows access to the device's registry information\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ThingName`  <a name="cfn-iotanalytics-pipeline-deviceregistryenrich-thingname"></a>
The name of the IoT device whose registry information is added to the message\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-deviceregistryenrich-seealso"></a>
+ [ RunPipelineActivity](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-runpipelineactivity) in the *AWS IoT Analytics User Guide*
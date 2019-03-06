# AWS IoT Analytics Pipeline RemoveAttributes<a name="aws-properties-iotanalytics-pipeline-removeattributes"></a>

<a name="aws-properties-iotanalytics-pipeline-removeattributes-description"></a>The `RemoveAttributes` property type specifies the attributes to remove from a message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-removeattributes-inheritance"></a> `RemoveAttributes` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-removeattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-removeattributes-syntax.json"></a>

```
{
  "[Attributes](#cfn-iotanalytics-pipeline-removeattributes-attributes)" : [ String, ... ],
  "[Name](#cfn-iotanalytics-pipeline-removeattributes-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-removeattributes-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-removeattributes-syntax.yaml"></a>

```
[Attributes](#cfn-iotanalytics-pipeline-removeattributes-attributes): 
  - String
[Name](#cfn-iotanalytics-pipeline-removeattributes-name): String
[Next](#cfn-iotanalytics-pipeline-removeattributes-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-removeattributes-properties"></a>

`Attributes`  <a name="cfn-iotanalytics-pipeline-removeattributes-attributes"></a>
Specifies the attributes to remove from the message\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-removeattributes-name"></a>
The name of the 'removeAttributes' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-removeattributes-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-removeattributes-seealso"></a>
+ [CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *IoT Analytics User Guide*
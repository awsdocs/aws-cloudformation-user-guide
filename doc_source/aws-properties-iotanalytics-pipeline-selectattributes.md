# AWS IoT Analytics Pipeline SelectAttributes<a name="aws-properties-iotanalytics-pipeline-selectattributes"></a>

<a name="aws-properties-iotanalytics-pipeline-selectattributes-description"></a>The `SelectAttributes` property type creates a new message using only the specified attributes from the original message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-selectattributes-inheritance"></a> `SelectAttributes` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-selectattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-selectattributes-syntax.json"></a>

```
{
  "[Attributes](#cfn-iotanalytics-pipeline-selectattributes-attributes)" : [ String, ... ],
  "[Name](#cfn-iotanalytics-pipeline-selectattributes-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-selectattributes-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-selectattributes-syntax.yaml"></a>

```
[Attributes](#cfn-iotanalytics-pipeline-selectattributes-attributes): 
  - String
[Name](#cfn-iotanalytics-pipeline-selectattributes-name): String
[Next](#cfn-iotanalytics-pipeline-selectattributes-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-selectattributes-properties"></a>

`Attributes`  <a name="cfn-iotanalytics-pipeline-selectattributes-attributes"></a>
A list of the attributes to select from the message\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-selectattributes-name"></a>
The name of the 'selectAttributes' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-selectattributes-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-selectattributes-seealso"></a>
+ [ CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *AWS IoT Analytics User Guide*
# AWS IoT Analytics Pipeline AddAttributes<a name="aws-properties-iotanalytics-pipeline-addattributes"></a>

<a name="aws-properties-iotanalytics-pipeline-addattributes-description"></a>The `AddAttributes` property type specifies additional attributes to be added to a message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-addattributes-inheritance"></a> `AddAttributes` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-addattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-addattributes-syntax.json"></a>

```
{
  "[Attributes](#cfn-iotanalytics-pipeline-addattributes-attributes)" : JSON object,
  "[Name](#cfn-iotanalytics-pipeline-addattributes-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-addattributes-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-addattributes-syntax.yaml"></a>

```
[Attributes](#cfn-iotanalytics-pipeline-addattributes-attributes): JSON object
[Name](#cfn-iotanalytics-pipeline-addattributes-name): String
[Next](#cfn-iotanalytics-pipeline-addattributes-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-addattributes-properties"></a>

`Attributes`  <a name="cfn-iotanalytics-pipeline-addattributes-attributes"></a>
A list of objects that map an existing attribute to a new attribute in a message\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-addattributes-name"></a>
The name of the 'addAttributes' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-addattributes-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-addattributes-seealso"></a>
+ [CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *AWS IoT Analytics User Guide\.*
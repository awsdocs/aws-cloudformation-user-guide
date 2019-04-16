# AWS IoT Analytics Pipeline Math<a name="aws-properties-iotanalytics-pipeline-math"></a>

<a name="aws-properties-iotanalytics-pipeline-math-description"></a>The `Math` property type specifies an arithmetic expression which is computed using the message's attributes and whose result is added to the message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-math-inheritance"></a> `Math` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-math-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-math-syntax.json"></a>

```
{
  "[Attribute](#cfn-iotanalytics-pipeline-math-attribute)" : String,
  "[Math](#cfn-iotanalytics-pipeline-math-math)" : String,
  "[Name](#cfn-iotanalytics-pipeline-math-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-math-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-math-syntax.yaml"></a>

```
[Attribute](#cfn-iotanalytics-pipeline-math-attribute): String
[Math](#cfn-iotanalytics-pipeline-math-math): String
[Name](#cfn-iotanalytics-pipeline-math-name): String
[Next](#cfn-iotanalytics-pipeline-math-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-math-properties"></a>

`Attribute`  <a name="cfn-iotanalytics-pipeline-math-attribute"></a>
The name of the attribute that will contain the result of the math operation\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Math`  <a name="cfn-iotanalytics-pipeline-math-math"></a>
An expression that uses one or more existing attributes and must return an integer value\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-math-name"></a>
The name of the 'math' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-math-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-math-seealso"></a>
+ [ CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *AWS IoT Analytics User Guide*
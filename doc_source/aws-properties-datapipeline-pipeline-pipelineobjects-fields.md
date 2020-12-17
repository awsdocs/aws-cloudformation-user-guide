# AWS::DataPipeline::Pipeline Field<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields"></a>

A key\-value pair that describes a property of a `PipelineObject`\. The value is specified as either a string value \(`StringValue`\) or a reference to another object \(`RefValue`\) but not as both\. To view fields for a data pipeline object, see [Pipeline Object Reference](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.

## Syntax<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields-syntax.json"></a>

```
{
  "[Key](#cfn-datapipeline-pipeline-pipelineobjects-fields-key)" : String,
  "[RefValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-refvalue)" : String,
  "[StringValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-stringvalue)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields-syntax.yaml"></a>

```
  [Key](#cfn-datapipeline-pipeline-pipelineobjects-fields-key): String
  [RefValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-refvalue): String
  [StringValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-stringvalue): 
    String
```

## Properties<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields-properties"></a>

`Key`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields-key"></a>
Specifies the name of a field for a particular object\. To view valid values for a particular field, see [Pipeline Object Reference](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefValue`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields-refvalue"></a>
A field value that you specify as an identifier of another object in the same pipeline definition\.  
You can specify the field value as either a string value \(`StringValue`\) or a reference to another object \(`RefValue`\), but not both\.
Required if the key that you are using requires it\.   
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValue`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields-stringvalue"></a>
A field value that you specify as a string\. To view valid values for a particular field, see [Pipeline Object Reference](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.  
You can specify the field value as either a string value \(`StringValue`\) or a reference to another object \(`RefValue`\), but not both\.
Required if the key that you are using requires it\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10240`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
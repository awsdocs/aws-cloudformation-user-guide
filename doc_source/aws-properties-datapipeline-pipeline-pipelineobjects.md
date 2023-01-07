# AWS::DataPipeline::Pipeline PipelineObject<a name="aws-properties-datapipeline-pipeline-pipelineobjects"></a>

PipelineObject is property of the AWS::DataPipeline::Pipeline resource that contains information about a pipeline object\. This can be a logical, physical, or physical attempt pipeline object\. The complete set of components of a pipeline defines the pipeline\.

## Syntax<a name="aws-properties-datapipeline-pipeline-pipelineobjects-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datapipeline-pipeline-pipelineobjects-syntax.json"></a>

```
{
  "[Fields](#cfn-datapipeline-pipeline-pipelineobjects-fields)" : [ Field, ... ],
  "[Id](#cfn-datapipeline-pipeline-pipelineobjects-id)" : String,
  "[Name](#cfn-datapipeline-pipeline-pipelineobjects-name)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-pipelineobjects-syntax.yaml"></a>

```
  [Fields](#cfn-datapipeline-pipeline-pipelineobjects-fields): 
    - Field
  [Id](#cfn-datapipeline-pipeline-pipelineobjects-id): String
  [Name](#cfn-datapipeline-pipeline-pipelineobjects-name): String
```

## Properties<a name="aws-properties-datapipeline-pipeline-pipelineobjects-properties"></a>

`Fields`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields"></a>
Key\-value pairs that define the properties of the object\.  
*Required*: Yes  
*Type*: List of [Field](aws-properties-datapipeline-pipeline-pipelineobjects-fields.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-datapipeline-pipeline-pipelineobjects-id"></a>
The ID of the object\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-datapipeline-pipeline-pipelineobjects-name"></a>
The name of the object\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
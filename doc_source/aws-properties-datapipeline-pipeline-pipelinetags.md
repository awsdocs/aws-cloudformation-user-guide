# AWS::DataPipeline::Pipeline PipelineTag<a name="aws-properties-datapipeline-pipeline-pipelinetags"></a>

A list of arbitrary tags \(key\-value pairs\) to associate with the pipeline, which you can use to control permissions\. For more information, see [Controlling Access to Pipelines and Resources](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-control-access.html) in the *AWS Data Pipeline Developer Guide*\. 

## Syntax<a name="aws-properties-datapipeline-pipeline-pipelinetags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datapipeline-pipeline-pipelinetags-syntax.json"></a>

```
{
  "[Key](#cfn-datapipeline-pipeline-pipelinetags-key)" : String,
  "[Value](#cfn-datapipeline-pipeline-pipelinetags-value)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-pipelinetags-syntax.yaml"></a>

```
  [Key](#cfn-datapipeline-pipeline-pipelinetags-key): String
  [Value](#cfn-datapipeline-pipeline-pipelinetags-value): String
```

## Properties<a name="aws-properties-datapipeline-pipeline-pipelinetags-properties"></a>

`Key`  <a name="cfn-datapipeline-pipeline-pipelinetags-key"></a>
The key name of a tag\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-datapipeline-pipeline-pipelinetags-value"></a>
The value to associate with the key name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
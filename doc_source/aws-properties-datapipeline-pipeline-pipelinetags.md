# AWS Data Pipeline Pipeline PipelineTags<a name="aws-properties-datapipeline-pipeline-pipelinetags"></a>

`PipelineTags` is a property of the [AWS::DataPipeline::Pipeline](aws-resource-datapipeline-pipeline.md) resource that defines arbitrary key\-value pairs for a pipeline\.

## Syntax<a name="w3ab2c21c14d574b5"></a>

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

## Properties<a name="w3ab2c21c14d574b7"></a>

`Key`  <a name="cfn-datapipeline-pipeline-pipelinetags-key"></a>
The key name of a tag\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-datapipeline-pipeline-pipelinetags-value"></a>
The value to associate with the key name\.  
*Required*: Yes  
*Type*: String
# AWS Data Pipeline Pipeline ParameterObjects<a name="aws-properties-datapipeline-pipeline-parameterobjects"></a>

`ParameterObjects` is a property of the [AWS::DataPipeline::Pipeline](aws-resource-datapipeline-pipeline.md) resource that describes parameters that are used in a pipeline definition\.

## Syntax<a name="w3ab2c21c14d554b5"></a>

### JSON<a name="aws-properties-datapipeline-pipeline-parameterobjects-syntax.json"></a>

```
{
  "[Attributes](#cfn-datapipeline-pipeline-parameterobjects-attributes)" : [ Attribute, ... ],
  "[Id](#cfn-datapipeline-pipeline-parameterobjects-id)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-parameterobjects-syntax.yaml"></a>

```
[Attributes](#cfn-datapipeline-pipeline-parameterobjects-attributes):
  - Attribute
[Id](#cfn-datapipeline-pipeline-parameterobjects-id): String
```

## Properties<a name="w3ab2c21c14d554b7"></a>

`Attributes`  <a name="cfn-datapipeline-pipeline-parameterobjects-attributes"></a>
Key\-value pairs that define the attributes of the parameter object\.  
*Required*: Yes  
*Type*: [AWS Data Pipeline Parameter Objects Attributes](aws-properties-datapipeline-pipeline-parameterobjects-attributes.md)

`Id`  <a name="cfn-datapipeline-pipeline-parameterobjects-id"></a>
The identifier of the parameter object\.  
*Required*: Yes  
*Type*: String
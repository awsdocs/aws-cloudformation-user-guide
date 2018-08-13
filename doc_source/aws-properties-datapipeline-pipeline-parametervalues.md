# AWS Data Pipeline Pipeline ParameterValues<a name="aws-properties-datapipeline-pipeline-parametervalues"></a>

`ParameterValues` is a property of the [AWS::DataPipeline::Pipeline](aws-resource-datapipeline-pipeline.md) resource that sets values for parameters that are used in a pipeline definition\.

## Syntax<a name="w3ab2c21c14d562b5"></a>

### JSON<a name="aws-properties-datapipeline-pipeline-parametervalues-syntax.json"></a>

```
{
  "[Id](#cfn-datapipeline-pipeline-parametervalues-id)" : String,
  "[StringValue](#cfn-datapipeline-pipeline-parametervalues-stringvalue)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-parametervalues-syntax.yaml"></a>

```
[Id](#cfn-datapipeline-pipeline-parametervalues-id): String
[StringValue](#cfn-datapipeline-pipeline-parametervalues-stringvalue): String
```

## Properties<a name="w3ab2c21c14d562b7"></a>

`Id`  <a name="cfn-datapipeline-pipeline-parametervalues-id"></a>
The ID of a parameter object\.  
*Required*: Yes  
*Type*: String

`StringValue`  <a name="cfn-datapipeline-pipeline-parametervalues-stringvalue"></a>
A value to associate with the parameter object\.  
*Required*: Yes  
*Type*: String
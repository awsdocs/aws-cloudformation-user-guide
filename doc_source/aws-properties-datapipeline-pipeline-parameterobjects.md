# AWS::DataPipeline::Pipeline ParameterObject<a name="aws-properties-datapipeline-pipeline-parameterobjects"></a>

Contains information about a parameter object\.

## Syntax<a name="aws-properties-datapipeline-pipeline-parameterobjects-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datapipeline-pipeline-parameterobjects-syntax.json"></a>

```
{
  "[Attributes](#cfn-datapipeline-pipeline-parameterobjects-attributes)" : [ ParameterAttribute, ... ],
  "[Id](#cfn-datapipeline-pipeline-parameterobjects-id)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-parameterobjects-syntax.yaml"></a>

```
  [Attributes](#cfn-datapipeline-pipeline-parameterobjects-attributes): 
    - ParameterAttribute
  [Id](#cfn-datapipeline-pipeline-parameterobjects-id): String
```

## Properties<a name="aws-properties-datapipeline-pipeline-parameterobjects-properties"></a>

`Attributes`  <a name="cfn-datapipeline-pipeline-parameterobjects-attributes"></a>
The attributes of the parameter object\.  
*Required*: Yes  
*Type*: List of [ParameterAttribute](aws-properties-datapipeline-pipeline-parameterobjects-attributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-datapipeline-pipeline-parameterobjects-id"></a>
The ID of the parameter object\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
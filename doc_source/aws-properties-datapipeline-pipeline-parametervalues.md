# AWS::DataPipeline::Pipeline ParameterValue<a name="aws-properties-datapipeline-pipeline-parametervalues"></a>

A value or list of parameter values\.

## Syntax<a name="aws-properties-datapipeline-pipeline-parametervalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
  [StringValue](#cfn-datapipeline-pipeline-parametervalues-stringvalue): 
    String
```

## Properties<a name="aws-properties-datapipeline-pipeline-parametervalues-properties"></a>

`Id`  <a name="cfn-datapipeline-pipeline-parametervalues-id"></a>
The ID of the parameter value\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValue`  <a name="cfn-datapipeline-pipeline-parametervalues-stringvalue"></a>
The field value, expressed as a String\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10240`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
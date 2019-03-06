# AWS IoT Analytics Dataset Variable<a name="aws-properties-iotanalytics-dataset-variable"></a>

<a name="aws-properties-iotanalytics-dataset-variable-description"></a>The `Variable` property type specifies the values of variables used within the context of the execution of the containerized application for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-variable-inheritance"></a> `Variable` is a property of the [ContainerAction](aws-properties-iotanalytics-dataset-containeraction.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-variable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-variable-syntax.json"></a>

```
{
  "[DatasetContentVersionValue](#cfn-iotanalytics-dataset-variable-datasetcontentversionvalue)" : [*DatasetContentVersionValue*](aws-properties-iotanalytics-dataset-datasetcontentversionvalue.md),
  "[DoubleValue](#cfn-iotanalytics-dataset-variable-doublevalue)" : Double,
  "[OutputFileUriValue](#cfn-iotanalytics-dataset-variable-outputfileurivalue)" : [*OutputFileUriValue*](aws-properties-iotanalytics-dataset-outputfileurivalue.md),
  "[StringValue](#cfn-iotanalytics-dataset-variable-stringvalue)" : String,
  "[VariableName](#cfn-iotanalytics-dataset-variable-variablename)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-variable-syntax.yaml"></a>

```
[DatasetContentVersionValue](#cfn-iotanalytics-dataset-variable-datasetcontentversionvalue): 
  [*DatasetContentVersionValue*](aws-properties-iotanalytics-dataset-datasetcontentversionvalue.md)
[DoubleValue](#cfn-iotanalytics-dataset-variable-doublevalue): Double
[OutputFileUriValue](#cfn-iotanalytics-dataset-variable-outputfileurivalue): 
  [*OutputFileUriValue*](aws-properties-iotanalytics-dataset-outputfileurivalue.md)
[StringValue](#cfn-iotanalytics-dataset-variable-stringvalue): String
[VariableName](#cfn-iotanalytics-dataset-variable-variablename): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-variable-properties"></a>

`DatasetContentVersionValue`  <a name="cfn-iotanalytics-dataset-variable-datasetcontentversionvalue"></a>
The value of the variable as a structure that specifies a data set content version\.  
 *Required*: No  
 *Type*: [*DatasetContentVersionValue*](aws-properties-iotanalytics-dataset-datasetcontentversionvalue.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DoubleValue`  <a name="cfn-iotanalytics-dataset-variable-doublevalue"></a>
The value of the variable as a Java "double" type\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OutputFileUriValue`  <a name="cfn-iotanalytics-dataset-variable-outputfileurivalue"></a>
The value of the variable as a structure that specifies an output file URI\.  
 *Required*: No  
 *Type*: [*OutputFileUriValue*](aws-properties-iotanalytics-dataset-outputfileurivalue.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StringValue`  <a name="cfn-iotanalytics-dataset-variable-stringvalue"></a>
The value of the variable as a Java "string" type\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VariableName`  <a name="cfn-iotanalytics-dataset-variable-variablename"></a>
The name of the variable\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-variable-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *IoT Analytics User Guide*
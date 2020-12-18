# AWS::IoTAnalytics::Dataset Variable<a name="aws-properties-iotanalytics-dataset-variable"></a>

An instance of a variable to be passed to the `containerAction` execution\. Each variable must have a name and a value given by one of `stringValue`, `datasetContentVersionValue`, or `outputFileUriValue`\.

## Syntax<a name="aws-properties-iotanalytics-dataset-variable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-variable-syntax.json"></a>

```
{
  "[DatasetContentVersionValue](#cfn-iotanalytics-dataset-variable-datasetcontentversionvalue)" : DatasetContentVersionValue,
  "[DoubleValue](#cfn-iotanalytics-dataset-variable-doublevalue)" : Double,
  "[OutputFileUriValue](#cfn-iotanalytics-dataset-variable-outputfileurivalue)" : OutputFileUriValue,
  "[StringValue](#cfn-iotanalytics-dataset-variable-stringvalue)" : String,
  "[VariableName](#cfn-iotanalytics-dataset-variable-variablename)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-variable-syntax.yaml"></a>

```
  [DatasetContentVersionValue](#cfn-iotanalytics-dataset-variable-datasetcontentversionvalue): 
    DatasetContentVersionValue
  [DoubleValue](#cfn-iotanalytics-dataset-variable-doublevalue): 
    Double
  [OutputFileUriValue](#cfn-iotanalytics-dataset-variable-outputfileurivalue): 
    OutputFileUriValue
  [StringValue](#cfn-iotanalytics-dataset-variable-stringvalue): 
    String
  [VariableName](#cfn-iotanalytics-dataset-variable-variablename): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-variable-properties"></a>

`DatasetContentVersionValue`  <a name="cfn-iotanalytics-dataset-variable-datasetcontentversionvalue"></a>
The value of the variable as a structure that specifies a dataset content version\.  
*Required*: No  
*Type*: [DatasetContentVersionValue](aws-properties-iotanalytics-dataset-variable-datasetcontentversionvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DoubleValue`  <a name="cfn-iotanalytics-dataset-variable-doublevalue"></a>
The value of the variable as a double \(numeric\)\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputFileUriValue`  <a name="cfn-iotanalytics-dataset-variable-outputfileurivalue"></a>
The value of the variable as a structure that specifies an output file URI\.  
*Required*: No  
*Type*: [OutputFileUriValue](aws-properties-iotanalytics-dataset-variable-outputfileurivalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValue`  <a name="cfn-iotanalytics-dataset-variable-stringvalue"></a>
The value of the variable as a string\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariableName`  <a name="cfn-iotanalytics-dataset-variable-variablename"></a>
The name of the variable\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
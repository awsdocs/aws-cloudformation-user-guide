# AWS IoT Analytics Dataset DatasetContentVersionValue<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue"></a>

<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-description"></a>The `DatasetContentVersionValue` property type specifies the value of a variable as a structure that specifies a data set content version for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-inheritance"></a> `DatasetContentVersionValue` is a property of the [Variable](aws-properties-iotanalytics-dataset-variable.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-syntax.json"></a>

```
{
  "[DatasetName](#cfn-iotanalytics-dataset-datasetcontentversionvalue-datasetname)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-syntax.yaml"></a>

```
[DatasetName](#cfn-iotanalytics-dataset-datasetcontentversionvalue-datasetname): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-properties"></a>

`DatasetName`  <a name="cfn-iotanalytics-dataset-datasetcontentversionvalue-datasetname"></a>
The data set whose latest contents will be used as input to the notebook or application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue-seealso"></a>
+ [ CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *IoT Analytics User Guide*
# AWS::IoTAnalytics::Dataset DatasetContentVersionValue<a name="aws-properties-iotanalytics-dataset-variable-datasetcontentversionvalue"></a>

The dataset whose latest contents are used as input to the notebook or application\.

## Syntax<a name="aws-properties-iotanalytics-dataset-variable-datasetcontentversionvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-variable-datasetcontentversionvalue-syntax.json"></a>

```
{
  "[DatasetName](#cfn-iotanalytics-dataset-variable-datasetcontentversionvalue-datasetname)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-variable-datasetcontentversionvalue-syntax.yaml"></a>

```
  [DatasetName](#cfn-iotanalytics-dataset-variable-datasetcontentversionvalue-datasetname): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-variable-datasetcontentversionvalue-properties"></a>

`DatasetName`  <a name="cfn-iotanalytics-dataset-variable-datasetcontentversionvalue-datasetname"></a>
The name of the dataset whose latest contents are used as input to the notebook or application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
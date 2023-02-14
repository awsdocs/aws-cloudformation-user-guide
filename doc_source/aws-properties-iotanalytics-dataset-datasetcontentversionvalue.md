# AWS::IoTAnalytics::Dataset DatasetContentVersionValue<a name="aws-properties-iotanalytics-dataset-datasetcontentversionvalue"></a>

The dataset whose latest contents are used as input to the notebook or application\.

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
The name of the dataset whose latest contents are used as input to the notebook or application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `(^(?!_{2}))(^[a-zA-Z0-9_]+$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
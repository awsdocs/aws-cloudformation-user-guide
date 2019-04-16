# AWS IoT Analytics Dataset TriggeringDataset<a name="aws-properties-iotanalytics-dataset-triggeringdataset"></a>

<a name="aws-properties-iotanalytics-dataset-triggeringdataset-description"></a>The `TriggeringDataset` property type specifies the data set whose content creation will trigger the creation of this data set's contents for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-triggeringdataset-inheritance"></a> `TriggeringDataset` is a property of the [Trigger](aws-properties-iotanalytics-dataset-trigger.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-triggeringdataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-triggeringdataset-syntax.json"></a>

```
{
  "[DatasetName](#cfn-iotanalytics-dataset-triggeringdataset-datasetname)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-triggeringdataset-syntax.yaml"></a>

```
[DatasetName](#cfn-iotanalytics-dataset-triggeringdataset-datasetname): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-triggeringdataset-properties"></a>

`DatasetName`  <a name="cfn-iotanalytics-dataset-triggeringdataset-datasetname"></a>
The name of the data set\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-triggeringdataset-seealso"></a>
+ [ CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *AWS IoT Analytics User Guide*
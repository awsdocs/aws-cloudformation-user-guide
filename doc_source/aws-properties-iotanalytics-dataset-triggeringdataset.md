# AWS::IoTAnalytics::Dataset TriggeringDataset<a name="aws-properties-iotanalytics-dataset-triggeringdataset"></a>

Information about the dataset whose content generation triggers the new dataset content generation\.

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
The name of the data set whose content generation triggers the new data set content generation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::IoTAnalytics::Dataset Trigger<a name="aws-properties-iotanalytics-dataset-trigger"></a>

The "DatasetTrigger" that specifies when the data set is automatically updated\.

## Syntax<a name="aws-properties-iotanalytics-dataset-trigger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-trigger-syntax.json"></a>

```
{
  "[Schedule](#cfn-iotanalytics-dataset-trigger-schedule)" : Schedule,
  "[TriggeringDataset](#cfn-iotanalytics-dataset-trigger-triggeringdataset)" : TriggeringDataset
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-trigger-syntax.yaml"></a>

```
  [Schedule](#cfn-iotanalytics-dataset-trigger-schedule): 
    Schedule
  [TriggeringDataset](#cfn-iotanalytics-dataset-trigger-triggeringdataset): 
    TriggeringDataset
```

## Properties<a name="aws-properties-iotanalytics-dataset-trigger-properties"></a>

`Schedule`  <a name="cfn-iotanalytics-dataset-trigger-schedule"></a>
The "Schedule" when the trigger is initiated\.  
*Required*: No  
*Type*: [Schedule](aws-properties-iotanalytics-dataset-trigger-schedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggeringDataset`  <a name="cfn-iotanalytics-dataset-trigger-triggeringdataset"></a>
Information about the data set whose content generation triggers the new data set content generation\.  
*Required*: No  
*Type*: [TriggeringDataset](aws-properties-iotanalytics-dataset-triggeringdataset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
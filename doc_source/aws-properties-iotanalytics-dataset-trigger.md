# AWS IoT Analytics Dataset Trigger<a name="aws-properties-iotanalytics-dataset-trigger"></a>

<a name="aws-properties-iotanalytics-dataset-trigger-description"></a>The `Trigger` property type specifies a list of triggers that cause data set contents to be populated at a specific time or when another data set's contents are created for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-trigger-inheritance"></a> `Trigger` is a property of the [AWS::IoTAnalytics::Dataset](aws-resource-iotanalytics-dataset.md) resource\.

## Syntax<a name="aws-properties-iotanalytics-dataset-trigger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-trigger-syntax.json"></a>

```
{
  "[Schedule](#cfn-iotanalytics-dataset-trigger-schedule)" : [*Schedule*](aws-properties-iotanalytics-dataset-schedule.md),
  "[TriggeringDataset](#cfn-iotanalytics-dataset-trigger-triggeringdataset)" : [*TriggeringDataset*](aws-properties-iotanalytics-dataset-triggeringdataset.md)
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-trigger-syntax.yaml"></a>

```
[Schedule](#cfn-iotanalytics-dataset-trigger-schedule): 
  [*Schedule*](aws-properties-iotanalytics-dataset-schedule.md)
[TriggeringDataset](#cfn-iotanalytics-dataset-trigger-triggeringdataset): 
  [*TriggeringDataset*](aws-properties-iotanalytics-dataset-triggeringdataset.md)
```

## Properties<a name="aws-properties-iotanalytics-dataset-trigger-properties"></a>

`Schedule`  <a name="cfn-iotanalytics-dataset-trigger-schedule"></a>
The schedule of when the trigger is initiated \(for triggering at a specific time\)\.  
 *Required*: No  
 *Type*: [*Schedule*](aws-properties-iotanalytics-dataset-schedule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TriggeringDataset`  <a name="cfn-iotanalytics-dataset-trigger-triggeringdataset"></a>
The data set whose content creation will trigger the creation of this data set's contents\.  
 *Required*: No  
 *Type*: [*TriggeringDataset*](aws-properties-iotanalytics-dataset-triggeringdataset.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-trigger-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *IoT Analytics User Guide*
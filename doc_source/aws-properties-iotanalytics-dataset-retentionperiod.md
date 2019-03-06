# AWS IoT Analytics Dataset RetentionPeriod<a name="aws-properties-iotanalytics-dataset-retentionperiod"></a>

<a name="aws-properties-iotanalytics-dataset-retentionperiod-description"></a>The `RetentionPeriod` property type specifies how long, in days, message data is kept for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-retentionperiod-inheritance"></a> `RetentionPeriod` is a property of the [AWS::IoTAnalytics::Dataset](aws-resource-iotanalytics-dataset.md) resource\.

## Syntax<a name="aws-properties-iotanalytics-dataset-retentionperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-retentionperiod-syntax.json"></a>

```
{
  "[NumberOfDays](#cfn-iotanalytics-dataset-retentionperiod-numberofdays)" : Integer,
  "[Unlimited](#cfn-iotanalytics-dataset-retentionperiod-unlimited)" : Boolean
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-retentionperiod-syntax.yaml"></a>

```
[NumberOfDays](#cfn-iotanalytics-dataset-retentionperiod-numberofdays): Integer
[Unlimited](#cfn-iotanalytics-dataset-retentionperiod-unlimited): Boolean
```

## Properties<a name="aws-properties-iotanalytics-dataset-retentionperiod-properties"></a>

`NumberOfDays`  <a name="cfn-iotanalytics-dataset-retentionperiod-numberofdays"></a>
The number of days that message data is kept\. The "unlimited" parameter must be false\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Unlimited`  <a name="cfn-iotanalytics-dataset-retentionperiod-unlimited"></a>
If true, message data is kept indefinitely\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-retentionperiod-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *IoT Analytics User Guide *
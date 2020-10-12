# AWS::IoTAnalytics::Dataset RetentionPeriod<a name="aws-properties-iotanalytics-dataset-retentionperiod"></a>

How long, in days, message data is kept\.

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
The number of days that message data is kept\. The `unlimited` parameter must be false\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unlimited`  <a name="cfn-iotanalytics-dataset-retentionperiod-unlimited"></a>
If true, message data is kept indefinitely\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
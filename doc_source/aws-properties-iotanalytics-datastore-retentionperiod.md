# AWS::IoTAnalytics::Datastore RetentionPeriod<a name="aws-properties-iotanalytics-datastore-retentionperiod"></a>

How long, in days, message data is kept\.

## Syntax<a name="aws-properties-iotanalytics-datastore-retentionperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-retentionperiod-syntax.json"></a>

```
{
  "[NumberOfDays](#cfn-iotanalytics-datastore-retentionperiod-numberofdays)" : Integer,
  "[Unlimited](#cfn-iotanalytics-datastore-retentionperiod-unlimited)" : Boolean
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-retentionperiod-syntax.yaml"></a>

```
  [NumberOfDays](#cfn-iotanalytics-datastore-retentionperiod-numberofdays): Integer
  [Unlimited](#cfn-iotanalytics-datastore-retentionperiod-unlimited): Boolean
```

## Properties<a name="aws-properties-iotanalytics-datastore-retentionperiod-properties"></a>

`NumberOfDays`  <a name="cfn-iotanalytics-datastore-retentionperiod-numberofdays"></a>
The number of days that message data is kept\. The `unlimited` parameter must be false\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unlimited`  <a name="cfn-iotanalytics-datastore-retentionperiod-unlimited"></a>
If true, message data is kept indefinitely\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
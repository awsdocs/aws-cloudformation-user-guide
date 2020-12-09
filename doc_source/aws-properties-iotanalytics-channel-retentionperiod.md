# AWS::IoTAnalytics::Channel RetentionPeriod<a name="aws-properties-iotanalytics-channel-retentionperiod"></a>

How long, in days, message data is kept\.

## Syntax<a name="aws-properties-iotanalytics-channel-retentionperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-channel-retentionperiod-syntax.json"></a>

```
{
  "[NumberOfDays](#cfn-iotanalytics-channel-retentionperiod-numberofdays)" : Integer,
  "[Unlimited](#cfn-iotanalytics-channel-retentionperiod-unlimited)" : Boolean
}
```

### YAML<a name="aws-properties-iotanalytics-channel-retentionperiod-syntax.yaml"></a>

```
  [NumberOfDays](#cfn-iotanalytics-channel-retentionperiod-numberofdays): Integer
  [Unlimited](#cfn-iotanalytics-channel-retentionperiod-unlimited): Boolean
```

## Properties<a name="aws-properties-iotanalytics-channel-retentionperiod-properties"></a>

`NumberOfDays`  <a name="cfn-iotanalytics-channel-retentionperiod-numberofdays"></a>
The number of days that message data is kept\. The `unlimited` parameter must be false\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unlimited`  <a name="cfn-iotanalytics-channel-retentionperiod-unlimited"></a>
If true, message data is kept indefinitely\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
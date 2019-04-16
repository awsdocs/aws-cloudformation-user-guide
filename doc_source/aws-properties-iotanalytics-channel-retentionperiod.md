# AWS IoT Analytics Channel RetentionPeriod<a name="aws-properties-iotanalytics-channel-retentionperiod"></a>

<a name="aws-properties-iotanalytics-channel-retentionperiod-description"></a>The `RetentionPeriod` property type specifies how long, in days, message data is kept for an AWS IoT Analytics channel\.

<a name="aws-properties-iotanalytics-channel-retentionperiod-inheritance"></a> `RetentionPeriod` is a property of the [AWS::IoTAnalytics::Channel](aws-resource-iotanalytics-channel.md) resource\.

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
The number of days that message data is kept\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Unlimited`  <a name="cfn-iotanalytics-channel-retentionperiod-unlimited"></a>
If true, message data is kept indefinitely\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-channel-retentionperiod-seealso"></a>
+ [ CreateChannel](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createchannel) in the *AWS IoT Analytics User Guide*
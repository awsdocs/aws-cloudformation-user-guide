# AWS IoT Analytics Datastore RetentionPeriod<a name="aws-properties-iotanalytics-datastore-retentionperiod"></a>

<a name="aws-properties-iotanalytics-datastore-retentionperiod-description"></a>The `RetentionPeriod` property type specifies how log, in days, message data is kept for an AWS IoT Analytics datastore\.

<a name="aws-properties-iotanalytics-datastore-retentionperiod-inheritance"></a> `RetentionPeriod` is a property of the [AWS::IoTAnalytics::Datastore](aws-resource-iotanalytics-datastore.md) resource\.

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
The number of days that message data is kept\. The "unlimited" parameter must be false\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Unlimited`  <a name="cfn-iotanalytics-datastore-retentionperiod-unlimited"></a>
If true, message data is kept indefinitely\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-datastore-retentionperiod-seealso"></a>
+ [ CreateDatastore](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdatastore) in the *AWS IoT Analytics User Guide*
# AWS::Timestream::ScheduledQuery NotificationConfiguration<a name="aws-properties-timestream-scheduledquery-notificationconfiguration"></a>

Notification configuration for a scheduled query\. A notification is sent by Timestream when a scheduled query is created, its state is updated or when it is deleted\. 

## Syntax<a name="aws-properties-timestream-scheduledquery-notificationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-scheduledquery-notificationconfiguration-syntax.json"></a>

```
{
  "[SnsConfiguration](#cfn-timestream-scheduledquery-notificationconfiguration-snsconfiguration)" : SnsConfiguration
}
```

### YAML<a name="aws-properties-timestream-scheduledquery-notificationconfiguration-syntax.yaml"></a>

```
  [SnsConfiguration](#cfn-timestream-scheduledquery-notificationconfiguration-snsconfiguration): 
    SnsConfiguration
```

## Properties<a name="aws-properties-timestream-scheduledquery-notificationconfiguration-properties"></a>

`SnsConfiguration`  <a name="cfn-timestream-scheduledquery-notificationconfiguration-snsconfiguration"></a>
Details on SNS configuration\.   
*Required*: Yes  
*Type*: [SnsConfiguration](aws-properties-timestream-scheduledquery-snsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
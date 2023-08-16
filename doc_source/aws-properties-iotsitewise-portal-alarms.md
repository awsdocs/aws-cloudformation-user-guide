# AWS::IoTSiteWise::Portal Alarms<a name="aws-properties-iotsitewise-portal-alarms"></a>

Contains the configuration information of an alarm created in an AWS IoT SiteWise Monitor portal\. You can use the alarm to monitor an asset property and get notified when the asset property value is outside a specified range\. For more information, see [Monitoring with alarms](https://docs.aws.amazon.com/iot-sitewise/latest/appguide/monitor-alarms.html) in the * AWS IoT SiteWise Application Guide*\.

## Syntax<a name="aws-properties-iotsitewise-portal-alarms-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-portal-alarms-syntax.json"></a>

```
{
  "[AlarmRoleArn](#cfn-iotsitewise-portal-alarms-alarmrolearn)" : String,
  "[NotificationLambdaArn](#cfn-iotsitewise-portal-alarms-notificationlambdaarn)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-portal-alarms-syntax.yaml"></a>

```
  [AlarmRoleArn](#cfn-iotsitewise-portal-alarms-alarmrolearn): String
  [NotificationLambdaArn](#cfn-iotsitewise-portal-alarms-notificationlambdaarn): String
```

## Properties<a name="aws-properties-iotsitewise-portal-alarms-properties"></a>

`AlarmRoleArn`  <a name="cfn-iotsitewise-portal-alarms-alarmrolearn"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the IAM role that allows the alarm to perform actions and access AWS resources and services, such as AWS IoT Events\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationLambdaArn`  <a name="cfn-iotsitewise-portal-alarms-notificationlambdaarn"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the Lambda function that manages alarm notifications\. For more information, see [Managing alarm notifications](https://docs.aws.amazon.com/iotevents/latest/developerguide/lambda-support.html) in the * AWS IoT Events Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
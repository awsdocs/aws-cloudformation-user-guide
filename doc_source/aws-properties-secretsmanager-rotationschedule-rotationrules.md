# AWS::SecretsManager::RotationSchedule RotationRules<a name="aws-properties-secretsmanager-rotationschedule-rotationrules"></a>

A structure that defines the rotation configuration for the secret\.

## Syntax<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-syntax.json"></a>

```
{
  "[AutomaticallyAfterDays](#cfn-secretsmanager-rotationschedule-rotationrules-automaticallyafterdays)" : Integer,
  "[Duration](#cfn-secretsmanager-rotationschedule-rotationrules-duration)" : String,
  "[ScheduleExpression](#cfn-secretsmanager-rotationschedule-rotationrules-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-syntax.yaml"></a>

```
  [AutomaticallyAfterDays](#cfn-secretsmanager-rotationschedule-rotationrules-automaticallyafterdays): Integer
  [Duration](#cfn-secretsmanager-rotationschedule-rotationrules-duration): String
  [ScheduleExpression](#cfn-secretsmanager-rotationschedule-rotationrules-scheduleexpression): String
```

## Properties<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-properties"></a>

`AutomaticallyAfterDays`  <a name="cfn-secretsmanager-rotationschedule-rotationrules-automaticallyafterdays"></a>
The number of days between automatic scheduled rotations of the secret\. You can use this value to check that your secret meets your compliance guidelines for how often secrets must be rotated\.  
In `DescribeSecret` and `ListSecrets`, this value is calculated from the rotation schedule after every successful rotation\. In `RotateSecret`, you can set the rotation schedule in `RotationRules` with `AutomaticallyAfterDays` or `ScheduleExpression`, but not both\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Duration`  <a name="cfn-secretsmanager-rotationschedule-rotationrules-duration"></a>
The length of the rotation window in hours, for example `3h` for a three hour window\. Secrets Manager rotates your secret at any time during this window\. The window must not go into the next UTC day\. If you don't specify this value, the window automatically ends at the end of the UTC day\. The window begins according to the `ScheduleExpression`\. For more information, including examples, see [Schedule expressions in Secrets Manager rotation](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotate-secrets_schedule.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `3`  
*Pattern*: `[0-9h]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-secretsmanager-rotationschedule-rotationrules-scheduleexpression"></a>
A `cron()` or `rate()` expression that defines the schedule for rotating your secret\. Secrets Manager rotation schedules use UTC time zone\.   
Secrets Manager `rate()` expressions represent the interval in days that you want to rotate your secret, for example `rate(10 days)`\. If you use a `rate()` expression, the rotation window opens at midnight, and Secrets Manager rotates your secret any time that day after midnight\. You can set a `Duration` to shorten the rotation window\.  
You can use a `cron()` expression to create rotation schedules that are more detailed than a rotation interval\. For more information, including examples, see [Schedule expressions in Secrets Manager rotation](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotate-secrets_schedule.html)\. If you use a `cron()` expression, Secrets Manager rotates your secret any time during that day after the window opens\. For example, `cron(0 8 1 * ? *)` represents a rotation window that occurs on the first day of every month beginning at 8:00 AM UTC\. Secrets Manager rotates the secret any time that day after 8:00 AM\. You can set a `Duration` to shorten the rotation window\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[0-9A-Za-z\(\)#\?\*\-\/, ]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-secretsmanager-rotationschedule-rotationrules--seealso"></a>
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [Rotate secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide
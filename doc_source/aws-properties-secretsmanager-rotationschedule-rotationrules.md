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
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-secretsmanager-rotationschedule-rotationrules-scheduleexpression"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-secretsmanager-rotationschedule-rotationrules--seealso"></a>
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [Rotate secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide
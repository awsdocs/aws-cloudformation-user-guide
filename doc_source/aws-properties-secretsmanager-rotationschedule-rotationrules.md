# AWS::SecretsManager::RotationSchedule RotationRules<a name="aws-properties-secretsmanager-rotationschedule-rotationrules"></a>

A structure that defines the rotation configuration for the secret\.

## Syntax<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-syntax.json"></a>

```
{
  "[AutomaticallyAfterDays](#cfn-secretsmanager-rotationschedule-rotationrules-automaticallyafterdays)" : Integer
}
```

### YAML<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-syntax.yaml"></a>

```
  [AutomaticallyAfterDays](#cfn-secretsmanager-rotationschedule-rotationrules-automaticallyafterdays): Integer
```

## Properties<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-properties"></a>

`AutomaticallyAfterDays`  <a name="cfn-secretsmanager-rotationschedule-rotationrules-automaticallyafterdays"></a>
Specifies the number of days between automatic scheduled rotations of the secret\.  
Secrets Manager schedules the next rotation when the previous one is complete\. Secrets Manager schedules the date by adding the rotation interval \(number of days\) to the actual date of the last rotation\. The service chooses the hour within that 24\-hour date window randomly\. The minute is also chosen somewhat randomly, but weighted towards the top of the hour and influenced by a variety of factors that help distribute load\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-secretsmanager-rotationschedule-rotationrules--seealso"></a>
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [Rotate secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide
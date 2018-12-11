# Secrets Manager RotationSchedule RotationRules<a name="aws-properties-secretsmanager-rotationschedule-rotationrules"></a>

<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-description"></a>The `RotationRules` property is used as part of the [AWS::SecretsManager::RotationSchedule](aws-resource-secretsmanager-rotationschedule.md) resource type to configure how and when Secrets Manager performs rotation for the associated secret\.

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
Specifies the number of days after the previous rotation before Secrets Manager triggers the next automatic rotation\.  
You can specify a minimum value of 1 and a maximum value of 1000\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-secretsmanager-rotationschedule-rotationrules-seealso"></a>
+ [AWS::SecretsManager::RotationSchedule](aws-resource-secretsmanager-rotationschedule.md)
+ [Rotating Your AWS Secrets Manager Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the *AWS Secrets Manager User Guide*
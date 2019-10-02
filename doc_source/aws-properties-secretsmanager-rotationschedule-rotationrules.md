# AWS::SecretsManager::RotationSchedule RotationRules<a name="aws-properties-secretsmanager-rotationschedule-rotationrules"></a>

 The `RotationRules` property is used as part of the [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html) resource type to configure how and when Secrets Manager performs rotation for the associated secret\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-secretsmanager-rotationschedule-rotationrules--seealso"></a>
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [Rotating Your AWS Secrets Manager Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`

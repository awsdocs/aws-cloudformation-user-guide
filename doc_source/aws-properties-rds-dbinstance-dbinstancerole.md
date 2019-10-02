# AWS::RDS::DBInstance DBInstanceRole<a name="aws-properties-rds-dbinstance-dbinstancerole"></a>

Describes an AWS Identity and Access Management \(IAM\) role that is associated with a DB instance\.

## Syntax<a name="aws-properties-rds-dbinstance-dbinstancerole-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbinstance-dbinstancerole-syntax.json"></a>

```
{
  "[FeatureName](#cfn-rds-dbinstance-dbinstancerole-featurename)" : String,
  "[RoleArn](#cfn-rds-dbinstance-dbinstancerole-rolearn)" : String,
  "[Status](#cfn-rds-dbinstance-dbinstancerole-status)" : String
}
```

### YAML<a name="aws-properties-rds-dbinstance-dbinstancerole-syntax.yaml"></a>

```
  [FeatureName](#cfn-rds-dbinstance-dbinstancerole-featurename): String
  [RoleArn](#cfn-rds-dbinstance-dbinstancerole-rolearn): String
  [Status](#cfn-rds-dbinstance-dbinstancerole-status): String
```

## Properties<a name="aws-properties-rds-dbinstance-dbinstancerole-properties"></a>

`FeatureName`  <a name="cfn-rds-dbinstance-dbinstancerole-featurename"></a>
The name of the feature associated with the AWS Identity and Access Management \(IAM\) role\. For the list of supported feature names, see `DBEngineVersion`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-rds-dbinstance-dbinstancerole-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that is associated with the DB instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-rds-dbinstance-dbinstancerole-status"></a>
Describes the state of association between the IAM role and the DB instance\. The Status property returns one of the following values:  
+  `ACTIVE` \- the IAM role ARN is associated with the DB instance and can be used to access other AWS services on your behalf\.
+  `PENDING` \- the IAM role ARN is being associated with the DB instance\.
+  `INVALID` \- the IAM role ARN is associated with the DB instance, but the DB instance is unable to assume the IAM role in order to access other AWS services on your behalf\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by ***all*** regions.
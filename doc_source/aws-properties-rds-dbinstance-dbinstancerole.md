# AWS::RDS::DBInstance DBInstanceRole<a name="aws-properties-rds-dbinstance-dbinstancerole"></a>

Describes an AWS Identity and Access Management \(IAM\) role that is associated with a DB instance\.

## Syntax<a name="aws-properties-rds-dbinstance-dbinstancerole-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbinstance-dbinstancerole-syntax.json"></a>

```
{
  "[FeatureName](#cfn-rds-dbinstance-dbinstancerole-featurename)" : String,
  "[RoleArn](#cfn-rds-dbinstance-dbinstancerole-rolearn)" : String
}
```

### YAML<a name="aws-properties-rds-dbinstance-dbinstancerole-syntax.yaml"></a>

```
  [FeatureName](#cfn-rds-dbinstance-dbinstancerole-featurename): String
  [RoleArn](#cfn-rds-dbinstance-dbinstancerole-rolearn): String
```

## Properties<a name="aws-properties-rds-dbinstance-dbinstancerole-properties"></a>

`FeatureName`  <a name="cfn-rds-dbinstance-dbinstancerole-featurename"></a>
The name of the feature associated with the AWS Identity and Access Management \(IAM\) role\. IAM roles that are associated with a DB instance grant permission for the DB instance to access other AWS services on your behalf\. For the list of supported feature names, see [DBEngineVersion](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_DBEngineVersion.html) in the *Amazon RDS API Reference*\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-rds-dbinstance-dbinstancerole-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that is associated with the DB instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
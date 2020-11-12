# AWS::RDS::DBCluster DBClusterRole<a name="aws-properties-rds-dbcluster-dbclusterrole"></a>

Describes an AWS Identity and Access Management \(IAM\) role that is associated with a DB cluster\.

## Syntax<a name="aws-properties-rds-dbcluster-dbclusterrole-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-dbclusterrole-syntax.json"></a>

```
{
  "[FeatureName](#cfn-rds-dbcluster-dbclusterrole-featurename)" : String,
  "[RoleArn](#cfn-rds-dbcluster-dbclusterrole-rolearn)" : String
}
```

### YAML<a name="aws-properties-rds-dbcluster-dbclusterrole-syntax.yaml"></a>

```
  [FeatureName](#cfn-rds-dbcluster-dbclusterrole-featurename): String
  [RoleArn](#cfn-rds-dbcluster-dbclusterrole-rolearn): String
```

## Properties<a name="aws-properties-rds-dbcluster-dbclusterrole-properties"></a>

`FeatureName`  <a name="cfn-rds-dbcluster-dbclusterrole-featurename"></a>
The name of the feature associated with the AWS Identity and Access Management \(IAM\) role\. IAM roles that are associated with a DB cluster grant permission for the DB cluster to access other AWS services on your behalf\. For the list of supported feature names, see [DBEngineVersion](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_DBEngineVersion.html) in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-rds-dbcluster-dbclusterrole-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that is associated with the DB cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
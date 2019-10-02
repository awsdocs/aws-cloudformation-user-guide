# AWS::RDS::DBCluster DBClusterRole<a name="aws-properties-rds-dbcluster-dbclusterrole"></a>

Describes an AWS Identity and Access Management \(IAM\) role that is associated with a DB cluster\.

## Syntax<a name="aws-properties-rds-dbcluster-dbclusterrole-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-dbclusterrole-syntax.json"></a>

```
{
  "[FeatureName](#cfn-rds-dbcluster-dbclusterrole-featurename)" : String,
  "[RoleArn](#cfn-rds-dbcluster-dbclusterrole-rolearn)" : String,
  "[Status](#cfn-rds-dbcluster-dbclusterrole-status)" : String
}
```

### YAML<a name="aws-properties-rds-dbcluster-dbclusterrole-syntax.yaml"></a>

```
  [FeatureName](#cfn-rds-dbcluster-dbclusterrole-featurename): String
  [RoleArn](#cfn-rds-dbcluster-dbclusterrole-rolearn): String
  [Status](#cfn-rds-dbcluster-dbclusterrole-status): String
```

## Properties<a name="aws-properties-rds-dbcluster-dbclusterrole-properties"></a>

`FeatureName`  <a name="cfn-rds-dbcluster-dbclusterrole-featurename"></a>
The name of the feature associated with the AWS Identity and Access Management \(IAM\) role\. For the list of supported feature names, see [DBEngineVersion](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_DBEngineVersion.html) in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-rds-dbcluster-dbclusterrole-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that is associated with the DB cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-rds-dbcluster-dbclusterrole-status"></a>
Describes the state of association between the IAM role and the DB cluster\. The Status property returns one of the following values:  
+  `ACTIVE` \- the IAM role ARN is associated with the DB cluster and can be used to access other AWS services on your behalf\.
+  `PENDING` \- the IAM role ARN is being associated with the DB cluster\.
+  `INVALID` \- the IAM role ARN is associated with the DB cluster, but the DB cluster is unable to assume the IAM role in order to access other AWS services on your behalf\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by ***all*** regions.
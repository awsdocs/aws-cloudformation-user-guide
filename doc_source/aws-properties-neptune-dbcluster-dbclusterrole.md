# AWS::Neptune::DBCluster DBClusterRole<a name="aws-properties-neptune-dbcluster-dbclusterrole"></a>

Describes an Amazon Identity and Access Management \(IAM\) role that is associated with a DB cluster\.

## Syntax<a name="aws-properties-neptune-dbcluster-dbclusterrole-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-neptune-dbcluster-dbclusterrole-syntax.json"></a>

```
{
  "[FeatureName](#cfn-neptune-dbcluster-dbclusterrole-featurename)" : String,
  "[RoleArn](#cfn-neptune-dbcluster-dbclusterrole-rolearn)" : String
}
```

### YAML<a name="aws-properties-neptune-dbcluster-dbclusterrole-syntax.yaml"></a>

```
  [FeatureName](#cfn-neptune-dbcluster-dbclusterrole-featurename): String
  [RoleArn](#cfn-neptune-dbcluster-dbclusterrole-rolearn): String
```

## Properties<a name="aws-properties-neptune-dbcluster-dbclusterrole-properties"></a>

`FeatureName`  <a name="cfn-neptune-dbcluster-dbclusterrole-featurename"></a>
The name of the feature associated with the Amazon Identity and Access Management \(IAM\) role\. For the list of supported feature names, see [DescribeDBEngineVersions](https://docs.aws.amazon.com/neptune/latest/userguide/api-other-apis.html#DescribeDBEngineVersions)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-neptune-dbcluster-dbclusterrole-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that is associated with the DB cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
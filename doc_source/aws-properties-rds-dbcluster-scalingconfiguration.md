# Amazon Relational Database Service DBCluster ScalingConfiguration<a name="aws-properties-rds-dbcluster-scalingconfiguration"></a>

<a name="aws-properties-rds-dbcluster-scalingconfiguration-description"></a>The `ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless DB cluster\.

<a name="aws-properties-rds-dbcluster-scalingconfiguration-inheritance"></a> `ScalingConfiguration` is a property of the [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md) resource type\.

## Syntax<a name="aws-properties-rds-dbcluster-scalingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-scalingconfiguration-syntax.json"></a>

```
{
  "[AutoPause](#cfn-rds-dbcluster-scalingconfiguration-autopause)" : Boolean,
  "[MaxCapacity](#cfn-rds-dbcluster-scalingconfiguration-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-rds-dbcluster-scalingconfiguration-mincapacity)" : Integer,
  "[SecondsBeforeAutoPause](#cfn-rds-dbcluster-scalingconfiguration-secondsbeforeautopause)" : Integer
}
```

### YAML<a name="aws-properties-rds-dbcluster-scalingconfiguration-syntax.yaml"></a>

```
[AutoPause](#cfn-rds-dbcluster-scalingconfiguration-autopause): Boolean
[MaxCapacity](#cfn-rds-dbcluster-scalingconfiguration-maxcapacity): Integer
[MinCapacity](#cfn-rds-dbcluster-scalingconfiguration-mincapacity): Integer
[SecondsBeforeAutoPause](#cfn-rds-dbcluster-scalingconfiguration-secondsbeforeautopause): Integer
```

## Properties<a name="aws-properties-rds-dbcluster-scalingconfiguration-properties"></a>

`AutoPause`  <a name="cfn-rds-dbcluster-scalingconfiguration-autopause"></a>
A value that specifies whether to allow or disallow automatic pause for an Aurora DB cluster in serverless DB engine mode\. A DB cluster can be paused only when it's idle \(it has no connections\)\.  
If a DB cluster is paused for more than seven days, the DB cluster might be backed up with a snapshot\. In this case, the DB cluster is restored when there is a request to connect to it\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MaxCapacity`  <a name="cfn-rds-dbcluster-scalingconfiguration-maxcapacity"></a>
The maximum capacity for an Aurora DB cluster in serverless DB engine mode\.  
Valid capacity values are 2, 4, 8, 16, 32, 64, 128, and 256\.  
The maximum capacity must be greater than or equal to the minimum capacity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MinCapacity`  <a name="cfn-rds-dbcluster-scalingconfiguration-mincapacity"></a>
The minimum capacity for an Aurora DB cluster in serverless DB engine mode\.  
Valid capacity values are 2, 4, 8, 16, 32, 64, 128, and 256\.  
The maximum capacity must be greater than or equal to the minimum capacity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SecondsBeforeAutoPause`  <a name="cfn-rds-dbcluster-scalingconfiguration-secondsbeforeautopause"></a>
The time, in seconds, before an Aurora DB cluster in `serverless` mode is paused\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-rds-dbcluster-scalingconfiguration-seealso"></a>
+ [ScalingConfiguration](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ScalingConfiguration.html) in the *Amazon RDS API Reference*
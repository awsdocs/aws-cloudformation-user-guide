# AWS::RDS::DBCluster ScalingConfiguration<a name="aws-properties-rds-dbcluster-scalingconfiguration"></a>

The `ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless DB cluster\. 

For more information, see [Using Amazon Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html) in the *Amazon Aurora User Guide*\.

This property is only supported for Aurora Serverless v1\. For Aurora Serverless v2, use `ServerlessV2ScalingConfiguration` property\.

Valid for: Aurora DB clusters only

## Syntax<a name="aws-properties-rds-dbcluster-scalingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-scalingconfiguration-syntax.json"></a>

```
{
  "[AutoPause](#cfn-rds-dbcluster-scalingconfiguration-autopause)" : Boolean,
  "[MaxCapacity](#cfn-rds-dbcluster-scalingconfiguration-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-rds-dbcluster-scalingconfiguration-mincapacity)" : Integer,
  "[SecondsBeforeTimeout](#cfn-rds-dbcluster-scalingconfiguration-secondsbeforetimeout)" : Integer,
  "[SecondsUntilAutoPause](#cfn-rds-dbcluster-scalingconfiguration-secondsuntilautopause)" : Integer,
  "[TimeoutAction](#cfn-rds-dbcluster-scalingconfiguration-timeoutaction)" : String
}
```

### YAML<a name="aws-properties-rds-dbcluster-scalingconfiguration-syntax.yaml"></a>

```
  [AutoPause](#cfn-rds-dbcluster-scalingconfiguration-autopause): Boolean
  [MaxCapacity](#cfn-rds-dbcluster-scalingconfiguration-maxcapacity): Integer
  [MinCapacity](#cfn-rds-dbcluster-scalingconfiguration-mincapacity): Integer
  [SecondsBeforeTimeout](#cfn-rds-dbcluster-scalingconfiguration-secondsbeforetimeout): Integer
  [SecondsUntilAutoPause](#cfn-rds-dbcluster-scalingconfiguration-secondsuntilautopause): Integer
  [TimeoutAction](#cfn-rds-dbcluster-scalingconfiguration-timeoutaction): String
```

## Properties<a name="aws-properties-rds-dbcluster-scalingconfiguration-properties"></a>

`AutoPause`  <a name="cfn-rds-dbcluster-scalingconfiguration-autopause"></a>
A value that indicates whether to allow or disallow automatic pause for an Aurora DB cluster in `serverless` DB engine mode\. A DB cluster can be paused only when it's idle \(it has no connections\)\.  
If a DB cluster is paused for more than seven days, the DB cluster might be backed up with a snapshot\. In this case, the DB cluster is restored when there is a request to connect to it\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCapacity`  <a name="cfn-rds-dbcluster-scalingconfiguration-maxcapacity"></a>
The maximum capacity for an Aurora DB cluster in `serverless` DB engine mode\.  
For Aurora MySQL, valid capacity values are `1`, `2`, `4`, `8`, `16`, `32`, `64`, `128`, and `256`\.  
For Aurora PostgreSQL, valid capacity values are `2`, `4`, `8`, `16`, `32`, `64`, `192`, and `384`\.  
The maximum capacity must be greater than or equal to the minimum capacity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-rds-dbcluster-scalingconfiguration-mincapacity"></a>
The minimum capacity for an Aurora DB cluster in `serverless` DB engine mode\.  
For Aurora MySQL, valid capacity values are `1`, `2`, `4`, `8`, `16`, `32`, `64`, `128`, and `256`\.  
For Aurora PostgreSQL, valid capacity values are `2`, `4`, `8`, `16`, `32`, `64`, `192`, and `384`\.  
The minimum capacity must be less than or equal to the maximum capacity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondsBeforeTimeout`  <a name="cfn-rds-dbcluster-scalingconfiguration-secondsbeforetimeout"></a>
The amount of time, in seconds, that Aurora Serverless v1 tries to find a scaling point to perform seamless scaling before enforcing the timeout action\. The default is 300\.  
Specify a value between 60 and 600 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondsUntilAutoPause`  <a name="cfn-rds-dbcluster-scalingconfiguration-secondsuntilautopause"></a>
The time, in seconds, before an Aurora DB cluster in `serverless` mode is paused\.  
Specify a value between 300 and 86,400 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutAction`  <a name="cfn-rds-dbcluster-scalingconfiguration-timeoutaction"></a>
The action to take when the timeout is reached, either `ForceApplyCapacityChange` or `RollbackCapacityChange`\.  
 `ForceApplyCapacityChange` sets the capacity to the specified value as soon as possible\.  
 `RollbackCapacityChange`, the default, ignores the capacity change if a scaling point isn't found in the timeout period\.  
If you specify `ForceApplyCapacityChange`, connections that prevent Aurora Serverless v1 from finding a scaling point might be dropped\.
For more information, see [ Autoscaling for Aurora Serverless v1](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.how-it-works.html#aurora-serverless.how-it-works.auto-scaling) in the *Amazon Aurora User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-rds-dbcluster-scalingconfiguration--examples"></a>



### <a name="aws-properties-rds-dbcluster-scalingconfiguration--examples--"></a>

The following specifies a scaling configuration\.

For a sample template that configures an Aurora Serverless DB cluster, see [ Creating an Amazon Aurora Serverless DB Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html#aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_DB_Cluster)\.

#### JSON<a name="aws-properties-rds-dbcluster-scalingconfiguration--examples----json"></a>

```
"ScalingConfiguration" : {
                  "AutoPause" : true,
                  "MinCapacity" : 4,
                  "MaxCapacity" : 32,
                  "SecondsUntilAutoPause" : 1000
              }
```

#### YAML<a name="aws-properties-rds-dbcluster-scalingconfiguration--examples----yaml"></a>

```
ScalingConfiguration:
        AutoPause: true
        MinCapacity: 4
        MaxCapacity: 32
        SecondsUntilAutoPause: 1000
```
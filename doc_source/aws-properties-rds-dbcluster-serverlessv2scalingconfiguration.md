# AWS::RDS::DBCluster ServerlessV2ScalingConfiguration<a name="aws-properties-rds-dbcluster-serverlessv2scalingconfiguration"></a>

The `ServerlessV2ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless V2 DB cluster\.

For more information, see [Using Amazon Aurora Serverless v2](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.html) in the *Amazon Aurora User Guide*\.

If you have an Aurora cluster, you must set the `ScalingConfigurationInfo` attribute before you add a DB instance that uses the `db.serverless` DB instance class\. For more information, see [Clusters that use Aurora Serverless v2 must have a capacity range specified](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.requirements.html#aurora-serverless-v2.requirements.capacity-range) in the *Amazon Aurora User Guide*\.

This property is only supported for Aurora Serverless v2\. For Aurora Serverless v1, use `ScalingConfiguration` property\.

## Syntax<a name="aws-properties-rds-dbcluster-serverlessv2scalingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-serverlessv2scalingconfiguration-syntax.json"></a>

```
{
  "[MaxCapacity](#cfn-rds-dbcluster-serverlessv2scalingconfiguration-maxcapacity)" : Double,
  "[MinCapacity](#cfn-rds-dbcluster-serverlessv2scalingconfiguration-mincapacity)" : Double
}
```

### YAML<a name="aws-properties-rds-dbcluster-serverlessv2scalingconfiguration-syntax.yaml"></a>

```
  [MaxCapacity](#cfn-rds-dbcluster-serverlessv2scalingconfiguration-maxcapacity): Double
  [MinCapacity](#cfn-rds-dbcluster-serverlessv2scalingconfiguration-mincapacity): Double
```

## Properties<a name="aws-properties-rds-dbcluster-serverlessv2scalingconfiguration-properties"></a>

`MaxCapacity`  <a name="cfn-rds-dbcluster-serverlessv2scalingconfiguration-maxcapacity"></a>
The maximum number of Aurora capacity units \(ACUs\) for a DB instance in an Aurora Serverless v2 cluster\. You can specify ACU values in half\-step increments, such as 40, 40\.5, 41, and so on\. The largest value that you can use is 128\.  
The maximum capacity must be higher than 0\.5 ACUs\. For more information, see [ Choosing the maximum Aurora Serverless v2 capacity setting for a cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.setting-capacity.html#aurora-serverless-v2.max_capacity_considerations) in the *Amazon Aurora User Guide*\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-rds-dbcluster-serverlessv2scalingconfiguration-mincapacity"></a>
The minimum number of Aurora capacity units \(ACUs\) for a DB instance in an Aurora Serverless v2 cluster\. You can specify ACU values in half\-step increments, such as 8, 8\.5, 9, and so on\. The smallest value that you can use is 0\.5\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
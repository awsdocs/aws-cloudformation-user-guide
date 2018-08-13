# Amazon EMR InstanceGroupConfig ScalingConstraints<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints"></a>

The `ScalingConstraints` property type specifies the upper and lower EC2 instance limits for an automatic scaling policy\. `ScalingConstraints` is the property type for the `Constraints` subproperty of the [Amazon EMR InstanceGroupConfig AutoScalingPolicy](aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy.md) property type\.

## Syntax<a name="w3ab2c21c14e1190b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints-syntax.json"></a>

```
{
  "[MaxCapacity](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-mincapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints-syntax.yaml"></a>

```
[MaxCapacity](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-maxcapacity): Integer
[MinCapacity](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-mincapacity): Integer
```

## Properties<a name="w3ab2c21c14e1190b7"></a>

`MaxCapacity`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-maxcapacity"></a>
For autoscaling, the maximum number of EC2 instances in an instance group\. Scale\-out activities add instances only up to this boundary\.  
*Required*: Yes  
*Type*: Integer

`MinCapacity`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-mincapacity"></a>
For autoscaling, the minimum number of EC2 instances in an instance group\. Scale\-in activities do not terminate instances below this boundary\.  
*Required*: Yes  
*Type*: Integer
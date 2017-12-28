# Amazon EMR InstanceGroupConfig ScalingConstraints<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints"></a>

The `ScalingConstraints` property type specifies the upper and lower EC2 instance limits for an automatic scaling policy\. `ScalingConstraints` is the property type for the `Constraints` subproperty of the [Amazon EMR InstanceGroupConfig AutoScalingPolicy](aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy.md) property type\.

## Syntax<a name="w3ab2c21c14d999b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-maxcapacity)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-mincapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-maxcapacity): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-mincapacity): Integer
```

## Properties<a name="w3ab2c21c14d999b7"></a>

`MaxCapacity`  
For autoscaling, the maximum number of EC2 instances in an instance group\. Scale\-out activities add instances only up to this boundary\.  
*Required: *Yes  
*Type*: Integer

`MinCapacity`  
For autoscaling, the minimum number of EC2 instances in an instance group\. Scale\-in activities do not terminate instances below this boundary\.  
*Required: *Yes  
*Type*: Integer
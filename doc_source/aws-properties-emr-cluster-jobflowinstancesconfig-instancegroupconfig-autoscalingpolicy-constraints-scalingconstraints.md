# Amazon EMR Cluster ScalingConstraints<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingconstraints"></a>

The `ScalingConstraints` property type specifies the upper and lower Amazon EC2 instance limits for an automatic scaling policy\. `ScalingConstraints` is the property type for the `Constraints` subproperty of the [Amazon EMR Cluster AutoScalingPolicy](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy.md) property type\.

## Syntax<a name="w3ab2c21c14e1117b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingconstraints-syntax.json"></a>

```
{
  "[MaxCapacity](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-mincapacity)" : Integer
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingconstraints-syntax.yaml"></a>

```
[MaxCapacity](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-maxcapacity): Integer
[MinCapacity](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-mincapacity): Integer
```

## Properties<a name="w3ab2c21c14e1117b7"></a>

`MaxCapacity`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-maxcapacity"></a>
The upper boundary of EC2 instances in an instance group beyond which scaling activities are not allowed to grow\. Scale\-out activities will not add instances beyond this boundary\.  
*Required*: Yes  
*Type*: Integer

`MinCapacity`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-mincapacity"></a>
The lower boundary of EC2 instances in an instance group below which scaling activities are not allowed to shrink\. Scale\-in activities will not terminate instances below this boundary\.  
*Required*: Yes  
*Type*: Integer
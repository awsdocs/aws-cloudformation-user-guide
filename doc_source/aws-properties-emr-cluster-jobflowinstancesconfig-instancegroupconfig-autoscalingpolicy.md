# Amazon EMR Cluster AutoScalingPolicy<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy"></a>

`AutoScalingPolicy` is a subproperty of the [Amazon EMR Cluster InstanceGroupConfig](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.md) property type that specifies the constraints and rules for an Auto Scaling group policy\. For more information, see [PutAutoScalingPolicy](http://docs.aws.amazon.com//ElasticMapReduce/latest/API/API_PutAutoScalingPolicy.html) in the Amazon EMR API Reference\.

## Syntax<a name="w3ab2c21c14e1063b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-syntax.json"></a>

```
{
  "[Constraints](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints)" : ScalingConstraints,
  "[Rules](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-rules)" : ScalingRule
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-syntax.yaml"></a>

```
[Constraints](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints): 
  - ScalingConstraints
[Rules](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-rules): 
  - ScalingRule
```

## Properties<a name="w3ab2c21c14e1063b7"></a>

`Constraints`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints"></a>
The upper and lower Amazon EC2 instance limits for an automatic scaling policy\. Automatic scaling activity will not cause an instance group to grow above or below these limits\.   
*Required*: Yes  
*Type*: [Amazon EMR Cluster ScalingConstraints](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingconstraints.md)

`Rules`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-rules"></a>
The scale\-in and scale\-out rules that comprise the automatic scaling policy\.  
*Required*: Yes  
*Type*: [Amazon EMR Cluster ScalingRule](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule.md)
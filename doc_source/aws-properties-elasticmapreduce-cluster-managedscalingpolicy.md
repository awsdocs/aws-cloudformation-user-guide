# AWS::EMR::Cluster ManagedScalingPolicy<a name="aws-properties-elasticmapreduce-cluster-managedscalingpolicy"></a>

 Managed scaling policy for an Amazon EMR cluster\. The policy specifies the limits for resources that can be added or terminated from a cluster\. The policy only applies to the core and task nodes\. The master node cannot be scaled after initial configuration\. 

## Syntax<a name="aws-properties-elasticmapreduce-cluster-managedscalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-managedscalingpolicy-syntax.json"></a>

```
{
  "[ComputeLimits](#cfn-elasticmapreduce-cluster-managedscalingpolicy-computelimits)" : ComputeLimits
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-managedscalingpolicy-syntax.yaml"></a>

```
  [ComputeLimits](#cfn-elasticmapreduce-cluster-managedscalingpolicy-computelimits): 
    ComputeLimits
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-managedscalingpolicy-properties"></a>

`ComputeLimits`  <a name="cfn-elasticmapreduce-cluster-managedscalingpolicy-computelimits"></a>
The EC2 unit limits for a managed scaling policy\. The managed scaling activity of a cluster is not allowed to go above or below these limits\. The limit only applies to the core and task nodes\. The master node cannot be scaled after initial configuration\.  
*Required*: No  
*Type*: [ComputeLimits](aws-properties-elasticmapreduce-cluster-computelimits.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
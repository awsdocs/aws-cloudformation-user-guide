# AWS::EMR::InstanceGroupConfig ScalingConstraints<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints"></a>

`ScalingConstraints` is a subproperty of the `AutoScalingPolicy` property type\. `ScalingConstraints` defines the upper and lower EC2 instance limits for an automatic scaling policy\. Automatic scaling activities triggered by automatic scaling rules will not cause an instance group to grow above or shrink below these limits\.

## Syntax<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints-properties"></a>

`MaxCapacity`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-maxcapacity"></a>
The upper boundary of EC2 instances in an instance group beyond which scaling activities are not allowed to grow\. Scale\-out activities will not add instances beyond this boundary\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingconstraints-mincapacity"></a>
The lower boundary of EC2 instances in an instance group below which scaling activities are not allowed to shrink\. Scale\-in activities will not terminate instances below this boundary\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::AutoScaling::WarmPool InstanceReusePolicy<a name="aws-properties-autoscaling-warmpool-instancereusepolicy"></a>

A structure that specifies an instance reuse policy for the `InstanceReusePolicy` property of the [AWS::AutoScaling::WarmPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-warmpool.html) resource\.

For more information, see [Warm pools for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-warm-pools.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-warmpool-instancereusepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-warmpool-instancereusepolicy-syntax.json"></a>

```
{
  "[ReuseOnScaleIn](#cfn-autoscaling-warmpool-instancereusepolicy-reuseonscalein)" : Boolean
}
```

### YAML<a name="aws-properties-autoscaling-warmpool-instancereusepolicy-syntax.yaml"></a>

```
  [ReuseOnScaleIn](#cfn-autoscaling-warmpool-instancereusepolicy-reuseonscalein): Boolean
```

## Properties<a name="aws-properties-autoscaling-warmpool-instancereusepolicy-properties"></a>

`ReuseOnScaleIn`  <a name="cfn-autoscaling-warmpool-instancereusepolicy-reuseonscalein"></a>
Specifies whether instances in the Auto Scaling group can be returned to the warm pool on scale in\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
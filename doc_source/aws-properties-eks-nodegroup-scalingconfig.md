# AWS::EKS::Nodegroup ScalingConfig<a name="aws-properties-eks-nodegroup-scalingconfig"></a>

An object representing the scaling configuration details for the Auto Scaling group that is associated with your node group\. If you specify a value for any property, then you must specify values for all of the properties\.

## Syntax<a name="aws-properties-eks-nodegroup-scalingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-nodegroup-scalingconfig-syntax.json"></a>

```
{
  "[DesiredSize](#cfn-eks-nodegroup-scalingconfig-desiredsize)" : Double,
  "[MaxSize](#cfn-eks-nodegroup-scalingconfig-maxsize)" : Double,
  "[MinSize](#cfn-eks-nodegroup-scalingconfig-minsize)" : Double
}
```

### YAML<a name="aws-properties-eks-nodegroup-scalingconfig-syntax.yaml"></a>

```
  [DesiredSize](#cfn-eks-nodegroup-scalingconfig-desiredsize): Double
  [MaxSize](#cfn-eks-nodegroup-scalingconfig-maxsize): Double
  [MinSize](#cfn-eks-nodegroup-scalingconfig-minsize): Double
```

## Properties<a name="aws-properties-eks-nodegroup-scalingconfig-properties"></a>

`DesiredSize`  <a name="cfn-eks-nodegroup-scalingconfig-desiredsize"></a>
The current number of worker nodes that the managed node group should maintain\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-eks-nodegroup-scalingconfig-maxsize"></a>
The maximum number of worker nodes that the managed node group can scale out to\. Managed node groups can support up to 100 nodes by default\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-eks-nodegroup-scalingconfig-minsize"></a>
The minimum number of worker nodes that the managed node group can scale in to\. This number must be greater than zero\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
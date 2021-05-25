# AWS::EKS::Nodegroup ScalingConfig<a name="aws-properties-eks-nodegroup-scalingconfig"></a>

An object representing the scaling configuration details for the Auto Scaling group that is associated with your node group\. When creating a node group, you must specify all or none of the properties\. When updating a node group, you can specify any or none of the properties\.

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
The current number of nodes that the managed node group should maintain\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-eks-nodegroup-scalingconfig-maxsize"></a>
The maximum number of nodes that the managed node group can scale out to\. For information about the maximum number that you can specify, see [Amazon EKS service quotas](https://docs.aws.amazon.com/eks/latest/userguide/service-quotas.html) in the *Amazon EKS User Guide*\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-eks-nodegroup-scalingconfig-minsize"></a>
The minimum number of nodes that the managed node group can scale in to\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
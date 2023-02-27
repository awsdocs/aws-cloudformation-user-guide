# AWS::EKS::Nodegroup ScalingConfig<a name="aws-properties-eks-nodegroup-scalingconfig"></a>

An object representing the scaling configuration details for the Auto Scaling group that is associated with your node group\. When creating a node group, you must specify all or none of the properties\. When updating a node group, you can specify any or none of the properties\.

## Syntax<a name="aws-properties-eks-nodegroup-scalingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-nodegroup-scalingconfig-syntax.json"></a>

```
{
  "[DesiredSize](#cfn-eks-nodegroup-scalingconfig-desiredsize)" : Integer,
  "[MaxSize](#cfn-eks-nodegroup-scalingconfig-maxsize)" : Integer,
  "[MinSize](#cfn-eks-nodegroup-scalingconfig-minsize)" : Integer
}
```

### YAML<a name="aws-properties-eks-nodegroup-scalingconfig-syntax.yaml"></a>

```
  [DesiredSize](#cfn-eks-nodegroup-scalingconfig-desiredsize): Integer
  [MaxSize](#cfn-eks-nodegroup-scalingconfig-maxsize): Integer
  [MinSize](#cfn-eks-nodegroup-scalingconfig-minsize): Integer
```

## Properties<a name="aws-properties-eks-nodegroup-scalingconfig-properties"></a>

`DesiredSize`  <a name="cfn-eks-nodegroup-scalingconfig-desiredsize"></a>
The current number of nodes that the managed node group should maintain\.  
If you use Cluster Autoscaler, you shouldn't change the desiredSize value directly, as this can cause the Cluster Autoscaler to suddenly scale up or scale down\.
Whenever this parameter changes, the number of worker nodes in the node group is updated to the specified size\. If this parameter is given a value that is smaller than the current number of running worker nodes, the necessary number of worker nodes are terminated to match the given value\. When using CloudFormation, no action occurs if you remove this parameter from your CFN template\.  
This parameter can be different from minSize in some cases, such as when starting with extra hosts for testing\. This parameter can also be different when you want to start with an estimated number of needed hosts, but let Cluster Autoscaler reduce the number if there are too many\. When Cluster Autoscaler is used, the desiredSize parameter is altered by Cluster Autoscaler \(but can be out\-of\-date for short periods of time\)\. Cluster Autoscaler doesn't scale a managed node group lower than minSize or higher than maxSize\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-eks-nodegroup-scalingconfig-maxsize"></a>
The maximum number of nodes that the managed node group can scale out to\. For information about the maximum number that you can specify, see [Amazon EKS service quotas](https://docs.aws.amazon.com/eks/latest/userguide/service-quotas.html) in the *Amazon EKS User Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-eks-nodegroup-scalingconfig-minsize"></a>
The minimum number of nodes that the managed node group can scale in to\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
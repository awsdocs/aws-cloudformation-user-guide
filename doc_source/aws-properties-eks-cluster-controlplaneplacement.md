# AWS::EKS::Cluster ControlPlanePlacement<a name="aws-properties-eks-cluster-controlplaneplacement"></a>

The placement configuration for all the control plane instances of your local Amazon EKS cluster on an AWS Outpost\. For more information, see [Capacity considerations](https://docs.aws.amazon.com/eks/latest/userguide/eks-outposts-capacity-considerations.html) in the Amazon EKS User Guide\.

## Syntax<a name="aws-properties-eks-cluster-controlplaneplacement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-controlplaneplacement-syntax.json"></a>

```
{
  "[GroupName](#cfn-eks-cluster-controlplaneplacement-groupname)" : String
}
```

### YAML<a name="aws-properties-eks-cluster-controlplaneplacement-syntax.yaml"></a>

```
  [GroupName](#cfn-eks-cluster-controlplaneplacement-groupname): String
```

## Properties<a name="aws-properties-eks-cluster-controlplaneplacement-properties"></a>

`GroupName`  <a name="cfn-eks-cluster-controlplaneplacement-groupname"></a>
The name of the placement group for the Kubernetes control plane instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
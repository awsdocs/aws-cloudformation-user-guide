# AWS::EKS::Cluster OutpostConfig<a name="aws-properties-eks-cluster-outpostconfig"></a>

The configuration of your local Amazon EKS cluster on an AWS Outpost\. Before creating a cluster on an Outpost, review [Creating a local cluster on an Outpost](https://docs.aws.amazon.com/eks/latest/userguide/eks-outposts-local-cluster-create.html) in the *Amazon EKS User Guide*\. This API isn't available for Amazon EKS clusters on the AWS cloud\.

## Syntax<a name="aws-properties-eks-cluster-outpostconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-outpostconfig-syntax.json"></a>

```
{
  "[ControlPlaneInstanceType](#cfn-eks-cluster-outpostconfig-controlplaneinstancetype)" : String,
  "[ControlPlanePlacement](#cfn-eks-cluster-outpostconfig-controlplaneplacement)" : ControlPlanePlacement,
  "[OutpostArns](#cfn-eks-cluster-outpostconfig-outpostarns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-eks-cluster-outpostconfig-syntax.yaml"></a>

```
  [ControlPlaneInstanceType](#cfn-eks-cluster-outpostconfig-controlplaneinstancetype): String
  [ControlPlanePlacement](#cfn-eks-cluster-outpostconfig-controlplaneplacement): 
    ControlPlanePlacement
  [OutpostArns](#cfn-eks-cluster-outpostconfig-outpostarns): 
    - String
```

## Properties<a name="aws-properties-eks-cluster-outpostconfig-properties"></a>

`ControlPlaneInstanceType`  <a name="cfn-eks-cluster-outpostconfig-controlplaneinstancetype"></a>
The Amazon EC2 instance type that you want to use for your local Amazon EKS cluster on Outposts\. Choose an instance type based on the number of nodes that your cluster will have\. For more information, see [Capacity considerations](https://docs.aws.amazon.com/eks/latest/userguide/eks-outposts-capacity-considerations.html) in the *Amazon EKS User Guide*\.  
The instance type that you specify is used for all Kubernetes control plane instances\. The instance type can't be changed after cluster creation\. The control plane is not automatically scaled by Amazon EKS\.  
   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ControlPlanePlacement`  <a name="cfn-eks-cluster-outpostconfig-controlplaneplacement"></a>
An object representing the placement configuration for all the control plane instances of your local Amazon EKS cluster on an AWS Outpost\. For more information, see [Capacity considerations](https://docs.aws.amazon.com/eks/latest/userguide/eks-outposts-capacity-considerations.html) in the *Amazon EKS User Guide*\.  
*Required*: No  
*Type*: [ControlPlanePlacement](aws-properties-eks-cluster-controlplaneplacement.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutpostArns`  <a name="cfn-eks-cluster-outpostconfig-outpostarns"></a>
The ARN of the Outpost that you want to use for your local Amazon EKS cluster on Outposts\. Only a single Outpost ARN is supported\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
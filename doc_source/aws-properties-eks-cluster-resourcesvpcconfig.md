# EKS Cluster ResourcesVpcConfig<a name="aws-properties-eks-cluster-resourcesvpcconfig"></a>

<a name="aws-properties-eks-cluster-resourcesvpcconfig-description"></a>The `ResourcesVpcConfig` property type specifies the VPC subnets and security groups used by the Amazon EKS cluster control plane\. Amazon EKS VPC resources have specific requirements to work properly with Kubernetes\. For more information, see [Cluster VPC Considerations](http://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html) and [Cluster Security Group Considerations](http://docs.aws.amazon.com/eks/latest/userguide/sec-group-reqs.html) in the *Amazon EKS User Guide*\.

<a name="aws-properties-eks-cluster-resourcesvpcconfig-inheritance"></a> `ResourcesVpcConfig` is a property of the [AWS::EKS::Cluster](aws-resource-eks-cluster.md) resource type\.

## Syntax<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-eks-cluster-resourcesvpcconfig-securitygroupids)" : [ String, ... ] ,
  "[SubnetIds](#cfn-eks-cluster-resourcesvpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax.yaml"></a>

```
[SecurityGroupIds](#cfn-eks-cluster-resourcesvpcconfig-securitygroupids)
  - String
[SubnetIds](#cfn-eks-cluster-resourcesvpcconfig-subnetids)
  - String
```

## Properties<a name="aws-properties-eks-cluster-resourcesvpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-securitygroupids"></a>
Specify one or more security groups for the cross\-account elastic network interfaces that Amazon EKS creates to use to allow communication between your worker nodes and the Kubernetes control plane\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-subnetids"></a>
Specify at least 2 subnets for your Amazon EKS worker nodes\. Amazon EKS creates cross\-account elastic network interfaces in these subnets to allow communication between your worker nodes and the Kubernetes control plane\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-eks-cluster-resourcesvpcconfig-seealso"></a>
+ [Clusters](http://docs.aws.amazon.com/eks/latest/userguide/clusters.html) in the *Amazon EKS User Guide*\.
+ [CreateCluster](http://docs.aws.amazon.com/eks/latest/APIReference/API_CreateCluster.html) in the *Amazon EKS API Reference*\.
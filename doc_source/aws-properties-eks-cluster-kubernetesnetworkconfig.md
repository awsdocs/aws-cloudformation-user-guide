# AWS::EKS::Cluster KubernetesNetworkConfig<a name="aws-properties-eks-cluster-kubernetesnetworkconfig"></a>

The Kubernetes network configuration for the cluster\.

## Syntax<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-syntax.json"></a>

```
{
  "[ServiceIpv4Cidr](#cfn-eks-cluster-kubernetesnetworkconfig-serviceipv4cidr)" : String
}
```

### YAML<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-syntax.yaml"></a>

```
  [ServiceIpv4Cidr](#cfn-eks-cluster-kubernetesnetworkconfig-serviceipv4cidr): String
```

## Properties<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-properties"></a>

`ServiceIpv4Cidr`  <a name="cfn-eks-cluster-kubernetesnetworkconfig-serviceipv4cidr"></a>
The CIDR block to assign Kubernetes service IP addresses from\. If you don't specify a block, Kubernetes assigns addresses from either the 10\.100\.0\.0/16 or 172\.20\.0\.0/16 CIDR blocks\. We recommend that you specify a block that does not overlap with resources in other networks that are peered or connected to your VPC\. The block must meet the following requirements:  
+ Within one of the following private IP address blocks: 10\.0\.0\.0/8, 172\.16\.0\.0\.0/12, or 192\.168\.0\.0/16\.
+ Doesn't overlap with any CIDR block assigned to the VPC that you selected for VPC\.
+ Between /24 and /12\.
You can only specify a custom CIDR block when you create a cluster and can't change this value once the cluster is created\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::EKS::Cluster KubernetesNetworkConfig<a name="aws-properties-eks-cluster-kubernetesnetworkconfig"></a>

The Kubernetes network configuration for the cluster\.

## Syntax<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-syntax.json"></a>

```
{
  "[IpFamily](#cfn-eks-cluster-kubernetesnetworkconfig-ipfamily)" : String,
  "[ServiceIpv4Cidr](#cfn-eks-cluster-kubernetesnetworkconfig-serviceipv4cidr)" : String,
  "[ServiceIpv6Cidr](#cfn-eks-cluster-kubernetesnetworkconfig-serviceipv6cidr)" : String
}
```

### YAML<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-syntax.yaml"></a>

```
  [IpFamily](#cfn-eks-cluster-kubernetesnetworkconfig-ipfamily): String
  [ServiceIpv4Cidr](#cfn-eks-cluster-kubernetesnetworkconfig-serviceipv4cidr): String
  [ServiceIpv6Cidr](#cfn-eks-cluster-kubernetesnetworkconfig-serviceipv6cidr): String
```

## Properties<a name="aws-properties-eks-cluster-kubernetesnetworkconfig-properties"></a>

`IpFamily`  <a name="cfn-eks-cluster-kubernetesnetworkconfig-ipfamily"></a>
Specify which IP family is used to assign Kubernetes pod and service IP addresses\. If you don't specify a value, `ipv4` is used by default\. You can only specify an IP family when you create a cluster and can't change this value once the cluster is created\. If you specify `ipv6`, the VPC and subnets that you specify for cluster creation must have both `IPv4` and `IPv6` CIDR blocks assigned to them\. You can't specify `ipv6` for clusters in China Regions\.  
You can only specify `ipv6` for `1.21` and later clusters that use version `1.10.1` or later of the Amazon VPC CNI add\-on\. If you specify `ipv6`, then ensure that your VPC meets the requirements listed in the considerations listed in [Assigning IPv6 addresses to pods and services](https://docs.aws.amazon.com/eks/latest/userguide/cni-ipv6.html) in the Amazon EKS User Guide\. Kubernetes assigns services `IPv6` addresses from the unique local address range `(fc00::/7)`\. You can't specify a custom `IPv6` CIDR block\. Pod addresses are assigned from the subnet's `IPv6` CIDR\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ipv4 | ipv6`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceIpv4Cidr`  <a name="cfn-eks-cluster-kubernetesnetworkconfig-serviceipv4cidr"></a>
Don't specify a value if you select `ipv6` for **ipFamily**\. The CIDR block to assign Kubernetes service IP addresses from\. If you don't specify a block, Kubernetes assigns addresses from either the `10.100.0.0/16` or `172.20.0.0/16` CIDR blocks\. We recommend that you specify a block that does not overlap with resources in other networks that are peered or connected to your VPC\. The block must meet the following requirements:  
+ Within one of the following private IP address blocks: `10.0.0.0/8`, `172.16.0.0/12`, or `192.168.0.0/16`\.
+ Doesn't overlap with any CIDR block assigned to the VPC that you selected for VPC\.
+ Between /24 and /12\.
You can only specify a custom CIDR block when you create a cluster and can't change this value once the cluster is created\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceIpv6Cidr`  <a name="cfn-eks-cluster-kubernetesnetworkconfig-serviceipv6cidr"></a>
The CIDR block that Kubernetes pod and service IP addresses are assigned from if you created a 1\.21 or later cluster with version 1\.10\.1 or later of the Amazon VPC CNI add\-on and specified `ipv6` for **ipFamily** when you created the cluster\. Kubernetes assigns service addresses from the unique local address range \(`fc00::/7`\) because you can't specify a custom IPv6 CIDR block when you create the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
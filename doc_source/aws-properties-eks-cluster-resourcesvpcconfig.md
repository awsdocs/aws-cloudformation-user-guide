# AWS::EKS::Cluster ResourcesVpcConfig<a name="aws-properties-eks-cluster-resourcesvpcconfig"></a>

An object representing the VPC configuration to use for an Amazon EKS cluster\.

**Important**  
When updating a resource, you must include these properties if the previous CloudFormation template of the resource had them:  
`EndpointPublicAccess`
`EndpointPrivateAccess`
`PublicAccessCidrs`

## Syntax<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax.json"></a>

```
{
  "[EndpointPrivateAccess](#cfn-eks-cluster-resourcesvpcconfig-endpointprivateaccess)" : Boolean,
  "[EndpointPublicAccess](#cfn-eks-cluster-resourcesvpcconfig-endpointpublicaccess)" : Boolean,
  "[PublicAccessCidrs](#cfn-eks-cluster-resourcesvpcconfig-publicaccesscidrs)" : [ String, ... ],
  "[SecurityGroupIds](#cfn-eks-cluster-resourcesvpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-eks-cluster-resourcesvpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax.yaml"></a>

```
  [EndpointPrivateAccess](#cfn-eks-cluster-resourcesvpcconfig-endpointprivateaccess): Boolean
  [EndpointPublicAccess](#cfn-eks-cluster-resourcesvpcconfig-endpointpublicaccess): Boolean
  [PublicAccessCidrs](#cfn-eks-cluster-resourcesvpcconfig-publicaccesscidrs): 
    - String
  [SecurityGroupIds](#cfn-eks-cluster-resourcesvpcconfig-securitygroupids): 
    - String
  [SubnetIds](#cfn-eks-cluster-resourcesvpcconfig-subnetids): 
    - String
```

## Properties<a name="aws-properties-eks-cluster-resourcesvpcconfig-properties"></a>

`EndpointPrivateAccess`  <a name="cfn-eks-cluster-resourcesvpcconfig-endpointprivateaccess"></a>
Set this value to `true` to enable private access for your cluster's Kubernetes API server endpoint\. If you enable private access, Kubernetes API requests from within your cluster's VPC use the private VPC endpoint\. The default value for this parameter is `false`, which disables private access for your Kubernetes API server\. If you disable private access and you have nodes or AWS Fargate pods in the cluster, then ensure that `publicAccessCidrs` includes the necessary CIDR blocks for communication with the nodes or Fargate pods\. For more information, see [Amazon EKS cluster endpoint access control](https://docs.aws.amazon.com/eks/latest/userguide/cluster-endpoint.html) in the * *Amazon EKS User Guide* *\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointPublicAccess`  <a name="cfn-eks-cluster-resourcesvpcconfig-endpointpublicaccess"></a>
Set this value to `false` to disable public access to your cluster's Kubernetes API server endpoint\. If you disable public access, your cluster's Kubernetes API server can only receive requests from within the cluster VPC\. The default value for this parameter is `true`, which enables public access for your Kubernetes API server\. For more information, see [Amazon EKS cluster endpoint access control](https://docs.aws.amazon.com/eks/latest/userguide/cluster-endpoint.html) in the * *Amazon EKS User Guide* *\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicAccessCidrs`  <a name="cfn-eks-cluster-resourcesvpcconfig-publicaccesscidrs"></a>
The CIDR blocks that are allowed access to your cluster's public Kubernetes API server endpoint\. Communication to the endpoint from addresses outside of the CIDR blocks that you specify is denied\. The default value is `0.0.0.0/0`\. If you've disabled private endpoint access and you have nodes or AWS Fargate pods in the cluster, then ensure that you specify the necessary CIDR blocks\. For more information, see [Amazon EKS cluster endpoint access control](https://docs.aws.amazon.com/eks/latest/userguide/cluster-endpoint.html) in the * *Amazon EKS User Guide* *\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-securitygroupids"></a>
Specify one or more security groups for the cross\-account elastic network interfaces that Amazon EKS creates to use that allow communication between your nodes and the Kubernetes control plane\. If you don't specify any security groups, then familiarize yourself with the difference between Amazon EKS defaults for clusters deployed with Kubernetes\. For more information, see [Amazon EKS security group considerations](https://docs.aws.amazon.com/eks/latest/userguide/sec-group-reqs.html) in the * *Amazon EKS User Guide* *\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-subnetids"></a>
Specify subnets for your Amazon EKS nodes\. Amazon EKS creates cross\-account elastic network interfaces in these subnets to allow communication between your nodes and the Kubernetes control plane\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
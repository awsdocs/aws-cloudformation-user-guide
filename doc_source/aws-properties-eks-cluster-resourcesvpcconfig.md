# AWS::EKS::Cluster ResourcesVpcConfig<a name="aws-properties-eks-cluster-resourcesvpcconfig"></a>

An object representing the VPC configuration to use for an Amazon EKS cluster\.

## Syntax<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-eks-cluster-resourcesvpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-eks-cluster-resourcesvpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-eks-cluster-resourcesvpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-eks-cluster-resourcesvpcconfig-securitygroupids): 
    - String
  [SubnetIds](#cfn-eks-cluster-resourcesvpcconfig-subnetids): 
    - String
```

## Properties<a name="aws-properties-eks-cluster-resourcesvpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-securitygroupids"></a>
Specify one or more security groups for the cross\-account elastic network interfaces that Amazon EKS creates to use to allow communication between your worker nodes and the Kubernetes control plane\. If you don't specify a security group, the default security group for your VPC is used\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-subnetids"></a>
Specify subnets for your Amazon EKS worker nodes\. Amazon EKS creates cross\-account elastic network interfaces in these subnets to allow communication between your worker nodes and the Kubernetes control plane\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
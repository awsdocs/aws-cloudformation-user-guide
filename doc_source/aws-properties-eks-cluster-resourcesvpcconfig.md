# AWS::EKS::Cluster ResourcesVpcConfig<a name="aws-properties-eks-cluster-resourcesvpcconfig"></a>

An object representing the VPC configuration to use for an Amazon EKS cluster\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointPublicAccess`  <a name="cfn-eks-cluster-resourcesvpcconfig-endpointpublicaccess"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicAccessCidrs`  <a name="cfn-eks-cluster-resourcesvpcconfig-publicaccesscidrs"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-securitygroupids"></a>
Specify one or more security groups for the cross\-account elastic network interfaces that Amazon EKS creates to use that allow communication between your nodes and the Kubernetes control plane\. If you don't specify any security groups, then familiarize yourself with the difference between Amazon EKS defaults for clusters deployed with Kubernetes:  
+ 1\.14 Amazon EKS platform version `eks.2` and earlier
+ 1\.14 Amazon EKS platform version `eks.3` and later 
For more information, see [Amazon EKS security group considerations](https://docs.aws.amazon.com/eks/latest/userguide/sec-group-reqs.html) in the * *Amazon EKS User Guide* *\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-eks-cluster-resourcesvpcconfig-subnetids"></a>
Specify subnets for your Amazon EKS nodes\. Amazon EKS creates cross\-account elastic network interfaces in these subnets to allow communication between your nodes and the Kubernetes control plane\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
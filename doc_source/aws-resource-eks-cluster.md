# AWS::EKS::Cluster<a name="aws-resource-eks-cluster"></a>

The `AWS::EKS::Cluster` resource creates an Amazon EKS cluster control plane\. The Amazon EKS cluster control plane consists of control plane instances that run the Kubernetes software, like `etcd` and the Kubernetes API server\. The control plane runs in an account managed by AWS, and the Kubernetes API is exposed via the Amazon EKS endpoint associated with your cluster\. For more information, see [Clusters](http://docs.aws.amazon.com/eks/latest/userguide/clusters.html) in the *Amazon EKS User Guide*\.

**Topics**
+ [Syntax](#aws-resource-eks-cluster-syntax)
+ [Properties](#aws-resource-eks-cluster-properties)
+ [Return Values](#aws-resource-eks-cluster-returnvalues)
+ [Examples](#aws-resource-eks-cluster-examples)
+ [See Also](#aws-resource-eks-cluster-seealso)

## Syntax<a name="aws-resource-eks-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eks-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::EKS::Cluster",
  "Properties" : {
    "[Name](#cfn-eks-cluster-name)" : String,
    "[ResourcesVpcConfig](#cfn-eks-cluster-resourcesvpcconfig)" : [EKS Cluster ResourcesVpcConfig](aws-properties-eks-cluster-resourcesvpcconfig.md),
    "[RoleArn](#cfn-eks-cluster-rolearn)" : String,
    "[Version](#cfn-eks-cluster-version)" : String
  }
}
```

### YAML<a name="aws-resource-eks-cluster-syntax.yaml"></a>

```
Type: "AWS::EKS::Cluster"
Properties:
  [Name](#cfn-eks-cluster-name): String
  [ResourcesVpcConfig](#cfn-eks-cluster-resourcesvpcconfig): [EKS Cluster ResourcesVpcConfig](aws-properties-eks-cluster-resourcesvpcconfig.md)
  [RoleArn](#cfn-eks-cluster-rolearn): String
  [Version](#cfn-eks-cluster-version): String
```

## Properties<a name="aws-resource-eks-cluster-properties"></a>

`Name`  <a name="cfn-eks-cluster-name"></a>
The name of the cluster\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourcesVpcConfig`  <a name="cfn-eks-cluster-resourcesvpcconfig"></a>
The VPC subnets and security groups used by the cluster control plane\. Amazon EKS VPC resources have specific requirements to work properly with Kubernetes\. For more information, see [Cluster VPC Considerations](http://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html) and [Cluster Security Group Considerations](http://docs.aws.amazon.com/eks/latest/userguide/sec-group-reqs.html) in the *Amazon EKS User Guide*\.  
 *Required*: Yes  
 *Type*: [EKS Cluster ResourcesVpcConfig](aws-properties-eks-cluster-resourcesvpcconfig.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RoleArn`  <a name="cfn-eks-cluster-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that provides permissions for the Kubernetes control plane to make calls to AWS API operations on your behalf\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Version`  <a name="cfn-eks-cluster-version"></a>
The Kubernetes server version for the cluster\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-eks-cluster-returnvalues"></a>

### Ref<a name="aws-resource-eks-cluster-ref"></a>

When you pass the logical ID of an `AWS::EKS::Cluster` resource to the intrinsic `Ref` function, the function returns the name of the cluster, such as `EKSCluster-NT5EUXTNTXXD`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-eks-cluster-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The ARN of the cluster, such as `arn:aws:eks:us-west-2:666666666666:cluster/prod`\. 

`CertificateAuthorityData`  
The `certificate-authority-data` for your cluster\. 

`Endpoint`  
The endpoint for your Kubernetes API server, such as `https://5E1D0CEXAMPLEA591B746AFC5AB30262.yl4.us-west-2.eks.amazonaws.com` 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-eks-cluster-examples"></a>

### Create a Cluster<a name="aws-resource-eks-cluster-example1"></a>

The following example creates an Amazon EKS cluster called `prod`\.

#### JSON<a name="aws-resource-eks-cluster-example1.json"></a>

```
{
  "Type": "AWS::EKS::Cluster",
  "Properties": {
    "Name": "prod",
    "Version": "1.10",
    "RoleArn": "arn:aws:iam::012345678910:role/eks-service-role-AWSServiceRoleForAmazonEKS-EXAMPLEBQ4PI",
    "ResourcesVpcConfig": {
      "SecurityGroupIds": [
        "sg-6979fe18"
      ],
      "SubnetIds": [
        "subnet-6782e71e",
        "subnet-e7e761ac"
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-eks-cluster-example1.yaml"></a>

```
Type: "AWS::EKS::Cluster"
Properties:
  Name: "prod"
  Version: "1.10"
  RoleArn: "arn:aws:iam::012345678910:role/eks-service-role-AWSServiceRoleForAmazonEKS-EXAMPLEBQ4PI"
  ResourcesVpcConfig:
    SecurityGroupIds: ["sg-6979fe18"]
    SubnetIds: ["subnet-6782e71e", "subnet-e7e761ac"]
```

## See Also<a name="aws-resource-eks-cluster-seealso"></a>
+ [Clusters](http://docs.aws.amazon.com/eks/latest/userguide/clusters.html) in the *Amazon EKS User Guide*\.
+ [CreateCluster](http://docs.aws.amazon.com/eks/latest/APIReference/API_CreateCluster.html) in the *Amazon EKS API Reference*\.
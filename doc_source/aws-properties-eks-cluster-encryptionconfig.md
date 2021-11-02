# AWS::EKS::Cluster EncryptionConfig<a name="aws-properties-eks-cluster-encryptionconfig"></a>

The encryption configuration for the cluster\.

## Syntax<a name="aws-properties-eks-cluster-encryptionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-encryptionconfig-syntax.json"></a>

```
{
  "[Provider](#cfn-eks-cluster-encryptionconfig-provider)" : Provider,
  "[Resources](#cfn-eks-cluster-encryptionconfig-resources)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-eks-cluster-encryptionconfig-syntax.yaml"></a>

```
  [Provider](#cfn-eks-cluster-encryptionconfig-provider): 
    Provider
  [Resources](#cfn-eks-cluster-encryptionconfig-resources): 
    - String
```

## Properties<a name="aws-properties-eks-cluster-encryptionconfig-properties"></a>

`Provider`  <a name="cfn-eks-cluster-encryptionconfig-provider"></a>
The encryption provider for the cluster\.  
*Required*: No  
*Type*: [Provider](aws-properties-eks-cluster-provider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resources`  <a name="cfn-eks-cluster-encryptionconfig-resources"></a>
Specifies the resources to be encrypted\. The only supported value is "secrets"\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
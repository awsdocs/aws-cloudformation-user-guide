# AWS::MSK::Cluster ConnectivityInfo<a name="aws-properties-msk-cluster-connectivityinfo"></a>

Specifies whether the cluster's brokers are publicly accessible\. By default, they are not\.

## Syntax<a name="aws-properties-msk-cluster-connectivityinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-connectivityinfo-syntax.json"></a>

```
{
  "[PublicAccess](#cfn-msk-cluster-connectivityinfo-publicaccess)" : PublicAccess,
  "[VpcConnectivity](#cfn-msk-cluster-connectivityinfo-vpcconnectivity)" : VpcConnectivity
}
```

### YAML<a name="aws-properties-msk-cluster-connectivityinfo-syntax.yaml"></a>

```
  [PublicAccess](#cfn-msk-cluster-connectivityinfo-publicaccess): 
    PublicAccess
  [VpcConnectivity](#cfn-msk-cluster-connectivityinfo-vpcconnectivity): 
    VpcConnectivity
```

## Properties<a name="aws-properties-msk-cluster-connectivityinfo-properties"></a>

`PublicAccess`  <a name="cfn-msk-cluster-connectivityinfo-publicaccess"></a>
Specifies whether the cluster's brokers are accessible from the internet\. Public access is off by default\.  
*Required*: No  
*Type*: [PublicAccess](aws-properties-msk-cluster-publicaccess.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConnectivity`  <a name="cfn-msk-cluster-connectivityinfo-vpcconnectivity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [VpcConnectivity](aws-properties-msk-cluster-vpcconnectivity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MSK::Cluster ConnectivityInfo<a name="aws-properties-msk-cluster-connectivityinfo"></a>

Broker access controls\.

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
Access control settings for the cluster's brokers\.  
*Required*: No  
*Type*: [PublicAccess](aws-properties-msk-cluster-publicaccess.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConnectivity`  <a name="cfn-msk-cluster-connectivityinfo-vpcconnectivity"></a>
VPC connection control settings for brokers  
*Required*: No  
*Type*: [VpcConnectivity](aws-properties-msk-cluster-vpcconnectivity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MSK::Cluster VpcConnectivityIam<a name="aws-properties-msk-cluster-vpcconnectivityiam"></a>

Details for SASL/IAM client authentication for VpcConnectivity\.

## Syntax<a name="aws-properties-msk-cluster-vpcconnectivityiam-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-vpcconnectivityiam-syntax.json"></a>

```
{
  "[Enabled](#cfn-msk-cluster-vpcconnectivityiam-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-vpcconnectivityiam-syntax.yaml"></a>

```
  [Enabled](#cfn-msk-cluster-vpcconnectivityiam-enabled): Boolean
```

## Properties<a name="aws-properties-msk-cluster-vpcconnectivityiam-properties"></a>

`Enabled`  <a name="cfn-msk-cluster-vpcconnectivityiam-enabled"></a>
SASL/IAM authentication is enabled or not\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
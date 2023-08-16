# AWS::MSK::Cluster VpcConnectivityTls<a name="aws-properties-msk-cluster-vpcconnectivitytls"></a>

Details for client authentication using TLS for vpcConnectivity\.

## Syntax<a name="aws-properties-msk-cluster-vpcconnectivitytls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-vpcconnectivitytls-syntax.json"></a>

```
{
  "[Enabled](#cfn-msk-cluster-vpcconnectivitytls-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-vpcconnectivitytls-syntax.yaml"></a>

```
  [Enabled](#cfn-msk-cluster-vpcconnectivitytls-enabled): Boolean
```

## Properties<a name="aws-properties-msk-cluster-vpcconnectivitytls-properties"></a>

`Enabled`  <a name="cfn-msk-cluster-vpcconnectivitytls-enabled"></a>
TLS authentication is enabled or not\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MSK::Cluster Tls<a name="aws-properties-msk-cluster-tls"></a>

Details for client authentication using TLS\.

## Syntax<a name="aws-properties-msk-cluster-tls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-tls-syntax.json"></a>

```
{
  "[CertificateAuthorityArnList](#cfn-msk-cluster-tls-certificateauthorityarnlist)" : [ String, ... ],
  "[Enabled](#cfn-msk-cluster-tls-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-tls-syntax.yaml"></a>

```
  [CertificateAuthorityArnList](#cfn-msk-cluster-tls-certificateauthorityarnlist): 
    - String
  [Enabled](#cfn-msk-cluster-tls-enabled): Boolean
```

## Properties<a name="aws-properties-msk-cluster-tls-properties"></a>

`CertificateAuthorityArnList`  <a name="cfn-msk-cluster-tls-certificateauthorityarnlist"></a>
List of ACM Certificate Authority ARNs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-msk-cluster-tls-enabled"></a>
TLS authentication is enabled or not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
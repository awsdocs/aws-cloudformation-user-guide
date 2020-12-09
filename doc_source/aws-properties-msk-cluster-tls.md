# AWS::MSK::Cluster Tls<a name="aws-properties-msk-cluster-tls"></a>

Details for client authentication using TLS\.

## Syntax<a name="aws-properties-msk-cluster-tls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-tls-syntax.json"></a>

```
{
  "[CertificateAuthorityArnList](#cfn-msk-cluster-tls-certificateauthorityarnlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-msk-cluster-tls-syntax.yaml"></a>

```
  [CertificateAuthorityArnList](#cfn-msk-cluster-tls-certificateauthorityarnlist): 
    - String
```

## Properties<a name="aws-properties-msk-cluster-tls-properties"></a>

`CertificateAuthorityArnList`  <a name="cfn-msk-cluster-tls-certificateauthorityarnlist"></a>
List of ACM Certificate Authority ARNs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
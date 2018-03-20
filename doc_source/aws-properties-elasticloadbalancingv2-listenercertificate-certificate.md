# Elastic Load Balancing ListenerCertificate Certificate<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate"></a>

<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate-description"></a>The `Certificate` property type specifies a certificate for an Elastic Load Balancing listener certificate\.

<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate-inheritance"></a> `Certificate` is a property of the [AWS::ElasticLoadBalancingV2::ListenerCertificate](aws-resource-elasticloadbalancingv2-listenercertificate.md) resource\. 

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-elasticloadbalancingv2-listenercertificate-certificate-certificatearn)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate-syntax.yaml"></a>

```
[CertificateArn](#cfn-elasticloadbalancingv2-listenercertificate-certificate-certificatearn): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenercertificate-certificate-properties"></a>

`CertificateArn`  <a name="cfn-elasticloadbalancingv2-listenercertificate-certificate-certificatearn"></a>
The Amazon Resource Name \(ARN\) of the certificate\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
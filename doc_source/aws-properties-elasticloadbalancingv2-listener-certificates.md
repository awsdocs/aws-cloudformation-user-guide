# Elastic Load Balancing V2 Certificate<a name="aws-properties-elasticloadbalancingv2-listener-certificates"></a>

The `Certificate` property type specifies the default server certificate that Elastic Load Balancing deploys on an HTTPS or TLS listener\. For more information, see [Create an HTTPS Listener for Your Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html) in the *User Guide for Application Load Balancers* or [Create a TLS Listener for Your Network Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/create-tls-listener.html) in the *User Guide for Network Load Balancers*\.

The `Certificates` property of the [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md) resource contains a list of one `Certificate` property type\.

## Syntax<a name="w13ab1c21c10d138c15c27b7"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-certificates-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-elasticloadbalancingv2-listener-certificates-certificatearn)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-certificates-syntax.yaml"></a>

```
[CertificateArn](#cfn-elasticloadbalancingv2-listener-certificates-certificatearn): String
```

## Properties<a name="w13ab1c21c10d138c15c27b9"></a>

`CertificateArn`  <a name="cfn-elasticloadbalancingv2-listener-certificates-certificatearn"></a>
The Amazon Resource Name \(ARN\) of the certificate\.  
*Required*: No  
*Type*: String
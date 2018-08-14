# Elastic Load Balancing Listener Certificate<a name="aws-properties-elasticloadbalancingv2-listener-certificates"></a>

The `Certificate` property type specifies the default SSL server certificate that Elastic Load Balancing will deploy on an listener\. For more information, see [Create an HTTPS Listener for Your Application Load Balancer](http://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html) in the *Application Load Balancers Guide*\.

The `Certificates` property of the [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md) resource contains a list of one `Certificate` property type\.

## Syntax<a name="w3ab2c21c14e1000b7"></a>

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

## Properties<a name="w3ab2c21c14e1000b9"></a>

`CertificateArn`  <a name="cfn-elasticloadbalancingv2-listener-certificates-certificatearn"></a>
The Amazon Resource Name \(ARN\) of the certificate to associate with the listener\.  
*Required*: No  
*Type*: String
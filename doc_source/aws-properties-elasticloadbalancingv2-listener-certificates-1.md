# AWS::ElasticLoadBalancingV2::Listener Certificate<a name="aws-properties-elasticloadbalancingv2-listener-certificates-1"></a>

Specifies an SSL server certificate for use with your load balancer\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-certificates-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-certificates-1-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-elasticloadbalancingv2-listener-certificates-certificatearn)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-certificates-1-syntax.yaml"></a>

```
  [CertificateArn](#cfn-elasticloadbalancingv2-listener-certificates-certificatearn): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-certificates-1-properties"></a>

`CertificateArn`  <a name="cfn-elasticloadbalancingv2-listener-certificates-certificatearn"></a>
The Amazon Resource Name \(ARN\) of the certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
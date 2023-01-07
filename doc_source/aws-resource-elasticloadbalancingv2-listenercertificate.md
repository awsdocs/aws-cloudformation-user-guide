# AWS::ElasticLoadBalancingV2::ListenerCertificate<a name="aws-resource-elasticloadbalancingv2-listenercertificate"></a>

Specifies an SSL server certificate to add to the certificate list for an HTTPS or TLS listener\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-listenercertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listenercertificate-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::ListenerCertificate",
  "Properties" : {
      "[Certificates](#cfn-elasticloadbalancingv2-listenercertificate-certificates)" : [ Certificate, ... ],
      "[ListenerArn](#cfn-elasticloadbalancingv2-listenercertificate-listenerarn)" : String
    }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listenercertificate-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::ListenerCertificate
Properties: 
  [Certificates](#cfn-elasticloadbalancingv2-listenercertificate-certificates): 
    - Certificate
  [ListenerArn](#cfn-elasticloadbalancingv2-listenercertificate-listenerarn): String
```

## Properties<a name="aws-resource-elasticloadbalancingv2-listenercertificate-properties"></a>

`Certificates`  <a name="cfn-elasticloadbalancingv2-listenercertificate-certificates"></a>
The certificate\. You can specify one certificate per resource\.  
*Required*: Yes  
*Type*: List of [Certificate](aws-properties-elasticloadbalancingv2-listener-certificates.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ListenerArn`  <a name="cfn-elasticloadbalancingv2-listenercertificate-listenerarn"></a>
The Amazon Resource Name \(ARN\) of the listener\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-resource-elasticloadbalancingv2-listenercertificate--seealso"></a>
+  [AddListenerCertificates](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_AddListenerCertificates.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [SSL Certificates](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html#https-listener-certificates) in the *User Guide for Application Load Balancers* 


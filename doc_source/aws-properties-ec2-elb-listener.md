# Elastic Load Balancing V1 Listener<a name="aws-properties-ec2-elb-listener"></a>

The `Listener` property is an embedded property of the `[AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)` type\. A listener is a process that checks for connection requests\. It is configured with a protocol and a port for front\-end \(client to load balancer\) connections, and a protocol and a port for back\-end \(load balancer to back\-end instance\) connections\. For more information, see [Listeners for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-listener-config.html) in the *User Guide for Classic Load Balancers*\.

## Syntax<a name="w13ab1c21c10d135c16c43b5"></a>

### JSON<a name="aws-properties-ec2-elb-listener-syntax.json"></a>

```
{
  "[InstancePort](#cfn-ec2-elb-listener-instanceport)" : String,
  "[InstanceProtocol](#cfn-ec2-elb-listener-instanceprotocol)" : String,
  "[LoadBalancerPort](#cfn-ec2-elb-listener-loadbalancerport)" : String,
  "[PolicyNames](#cfn-ec2-elb-listener-policynames)" :  [ String, ... ],
  "[Protocol](#cfn-ec2-elb-listener-protocol)" : String,
  "[SSLCertificateId](#cfn-ec2-elb-listener-sslcertificateid)" : String
}
```

### YAML<a name="aws-properties-ec2-elb-listener-syntax.yaml"></a>

```
[InstancePort](#cfn-ec2-elb-listener-instanceport): String
[InstanceProtocol](#cfn-ec2-elb-listener-instanceprotocol): String
[LoadBalancerPort](#cfn-ec2-elb-listener-loadbalancerport): String
[PolicyNames](#cfn-ec2-elb-listener-policynames):
  - String
[Protocol](#cfn-ec2-elb-listener-protocol): String
[SSLCertificateId](#cfn-ec2-elb-listener-sslcertificateid): String
```

## Properties<a name="w13ab1c21c10d135c16c43b7"></a>

`InstancePort`  <a name="cfn-ec2-elb-listener-instanceport"></a>
The TCP port on which the instance server listens\. You can't modify this property during the life of the load balancer\.  
*Required*: Yes  
*Type*: String

`InstanceProtocol`  <a name="cfn-ec2-elb-listener-instanceprotocol"></a>
The protocol to use for routing traffic to back\-end instances: HTTP, HTTPS, TCP, or SSL\. You can't modify this property during the life of the load balancer\.  
+ If the front\-end protocol is HTTP or HTTPS, `InstanceProtocol` must be on the same protocol layer \(HTTP or HTTPS\)\. Likewise, if the front\-end protocol is TCP or SSL, `InstanceProtocol` must be TCP or SSL\. By default, Elastic Load Balancing sets the instance protocol to HTTP or TCP\.
+ If there is another `Listener` with the same `InstancePort` whose `InstanceProtocol` is secure, \(using HTTPS or SSL\), the `InstanceProtocol` of the `Listener` must be secure \(using HTTPS or SSL\)\. If there is another `Listener` with the same `InstancePort` whose `InstanceProtocol` is HTTP or TCP, the `InstanceProtocol` of the `Listener` must be either HTTP or TCP\.
*Required*: No  
*Type*: String

`LoadBalancerPort`  <a name="cfn-ec2-elb-listener-loadbalancerport"></a>
The load balancer port number\. You can't modify this property during the life of the load balancer\.  
*Required*: Yes  
*Type*: String

`PolicyNames`  <a name="cfn-ec2-elb-listener-policynames"></a>
The [`ElasticLoadBalancing` policies](aws-properties-ec2-elb-policy.md) to associate with the `Listener`\. Specify only policies that are compatible with a `Listener`\. For more information, see `[DescribeLoadBalancerPolicyTypes](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_DescribeLoadBalancerPolicyTypes.html)` in the *Elastic Load Balancing API Reference version 2012\-06\-01*\.  
By default, Elastic Load Balancing associates the latest predefined policy with your load balancer\. When a new predefined policy is added, we recommend that you update your load balancer to use the new predefined policy\. Alternatively, you can select a different predefined security policy or create a custom policy\. To create a security policy, use the `Policies` property of the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\.
*Required*: No  
*Type*: List of String values

`Protocol`  <a name="cfn-ec2-elb-listener-protocol"></a>
The load balancer transport protocol to use for routing: HTTP, HTTPS, TCP or SSL\. You can't modify this property during the life of the load balancer\.  
*Required*: Yes  
*Type*: String

`SSLCertificateId`  <a name="cfn-ec2-elb-listener-sslcertificateid"></a>
The ARN of the SSL certificate to use for HTTPS or SSL listeners\. For more information, see [SSL/TLS Certificates for Classic Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/ssl-server-cert.html) in the *User Guide for Classic Load Balancers*\.  
*Required*: No  
*Type*: String
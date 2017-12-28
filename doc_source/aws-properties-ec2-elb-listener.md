# ElasticLoadBalancing Listener Property Type<a name="aws-properties-ec2-elb-listener"></a>

The `Listener` property is an embedded property of the `AWS::ElasticLoadBalancing::LoadBalancer` type\.

## Syntax<a name="w3ab2c21c14d805b5"></a>

### JSON<a name="aws-properties-ec2-elb-listener-syntax.json"></a>

```
{
  "InstancePort" : String,
  "InstanceProtocol" : String,
  "LoadBalancerPort" : String,
  "PolicyNames" :  [ String, ... ],
  "Protocol" : String,
  "SSLCertificateId" : String
}
```

### YAML<a name="aws-properties-ec2-elb-listener-syntax.yaml"></a>

```
InstancePort: String
InstanceProtocol: String
LoadBalancerPort: String
PolicyNames:
  - String
Protocol: String
SSLCertificateId: String
```

## Properties<a name="w3ab2c21c14d805b7"></a>

`InstancePort`  
Specifies the TCP port on which the instance server listens\. You can't modify this property during the life of the load balancer\.  
*Required: *Yes  
*Type*: String

`InstanceProtocol`  
Specifies the protocol to use for routing traffic to back\-end instances: HTTP, HTTPS, TCP, or SSL\. You can't modify this property during the life of the load balancer\.  
*Required: *No  
*Type*: String  

+ If the front\-end protocol is HTTP or HTTPS, `InstanceProtocol` must be on the same protocol layer \(HTTP or HTTPS\)\. Likewise, if the front\-end protocol is TCP or SSL, `InstanceProtocol` must be TCP or SSL\. By default, Elastic Load Balancing sets the instance protocol to HTTP or TCP\.

+ If there is another `Listener` with the same `InstancePort` whose `InstanceProtocol` is secure, \(using HTTPS or SSL\), the `InstanceProtocol` of the `Listener` must be secure \(using HTTPS or SSL\)\. If there is another `Listener` with the same `InstancePort` whose `InstanceProtocol` is HTTP or TCP, the `InstanceProtocol` of the `Listener` must be either HTTP or TCP\.

`LoadBalancerPort`  
Specifies the external load balancer port number\. You can't modify this property during the life of the load balancer\.  
*Required: *Yes  
*Type*: String

`PolicyNames`  
A list of `ElasticLoadBalancing` policy names to associate with the `Listener`\. Specify only policies that are compatible with a `Listener`\. For more information, see `[DescribeLoadBalancerPolicyTypes](http://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_DescribeLoadBalancerPolicyTypes.html)` in the *Elastic Load Balancing API Reference version 2012\-06\-01*\.  
By default, Elastic Load Balancing associates the latest predefined policy with your load balancer\. When a new predefined policy is added, we recommend that you update your load balancer to use the new predefined policy\. Alternatively, you can select a different predefined security policy or create a custom policy\. To create a security policy, use the `Policies` property of the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\.
*Required: *No  
*Type*: List of String values

`Protocol`  
Specifies the load balancer transport protocol to use for routing: HTTP, HTTPS, TCP or SSL\. You can't modify this property during the life of the load balancer\.  
*Required: *Yes  
*Type*: String

`SSLCertificateId`  
The ARN of the SSL certificate to use\. For more information about SSL certificates, see [Managing Server Certificates](http://docs.aws.amazon.com/IAM/latest/UserGuide/ManagingServerCerts.html) in the *AWS Identity and Access Management User Guide*\.  
*Required: *No  
*Type*: String
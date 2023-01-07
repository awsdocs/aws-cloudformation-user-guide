# AWS::ElasticLoadBalancing::LoadBalancer Listeners<a name="aws-properties-ec2-elb-listener"></a>

Specifies a listener for your Classic Load Balancer\.

## Syntax<a name="aws-properties-ec2-elb-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-elb-listener-syntax.json"></a>

```
{
  "[InstancePort](#cfn-ec2-elb-listener-instanceport)" : String,
  "[InstanceProtocol](#cfn-ec2-elb-listener-instanceprotocol)" : String,
  "[LoadBalancerPort](#cfn-ec2-elb-listener-loadbalancerport)" : String,
  "[PolicyNames](#cfn-ec2-elb-listener-policynames)" : [ String, ... ],
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

## Properties<a name="aws-properties-ec2-elb-listener-properties"></a>

`InstancePort`  <a name="cfn-ec2-elb-listener-instanceport"></a>
The port on which the instance is listening\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceProtocol`  <a name="cfn-ec2-elb-listener-instanceprotocol"></a>
The protocol to use for routing traffic to instances: HTTP, HTTPS, TCP, or SSL\.  
If the front\-end protocol is TCP or SSL, the back\-end protocol must be TCP or SSL\. If the front\-end protocol is HTTP or HTTPS, the back\-end protocol must be HTTP or HTTPS\.  
If there is another listener with the same `InstancePort` whose `InstanceProtocol` is secure, \(HTTPS or SSL\), the listener's `InstanceProtocol` must also be secure\.  
If there is another listener with the same `InstancePort` whose `InstanceProtocol` is HTTP or TCP, the listener's `InstanceProtocol` must be HTTP or TCP\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerPort`  <a name="cfn-ec2-elb-listener-loadbalancerport"></a>
The port on which the load balancer is listening\. On EC2\-VPC, you can specify any port from the range 1\-65535\. On EC2\-Classic, you can specify any port from the following list: 25, 80, 443, 465, 587, 1024\-65535\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyNames`  <a name="cfn-ec2-elb-listener-policynames"></a>
The names of the policies to associate with the listener\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-elb-listener-protocol"></a>
The load balancer transport protocol to use for routing: HTTP, HTTPS, TCP, or SSL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSLCertificateId`  <a name="cfn-ec2-elb-listener-sslcertificateid"></a>
The Amazon Resource Name \(ARN\) of the server certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-elb-listener--seealso"></a>
+  [CreateLoadBalancerListeners](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_CreateLoadBalancerListeners.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-listener-config.html) in the *User Guide for Classic Load Balancers* 
+  [HTTPS Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-https-load-balancers.html) in the *User Guide for Classic Load Balancers* 


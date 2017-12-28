# ElasticLoadBalancing Policy Type<a name="aws-properties-ec2-elb-policy"></a>

The ElasticLoadBalancing policy type is an embedded property of the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\. You associate policies with a listener by referencing a policy's name in the listener's `PolicyNames` property\.

## Syntax<a name="w3ab2c21c14d809b5"></a>

### JSON<a name="aws-properties-ec2-elb-policy-syntax.json"></a>

```
{
  "Attributes" : [ { "Name" : String, "Value" : String }, ... ],
  "InstancePorts" : [ String, ... ],
  "LoadBalancerPorts" : [ String, ... ],
  "PolicyName" : String,
  "PolicyType" : String
}
```

### YAML<a name="aws-properties-ec2-elb-policy-syntax.yaml"></a>

```
Attributes:
  -
    "Name" : String
    "Value" : String
InstancePorts:
  - String
LoadBalancerPorts:
  - String
PolicyName: String
PolicyType: String
```

## Properties<a name="w3ab2c21c14d809b7"></a>

`Attributes`  
A list of arbitrary attributes for this policy\. If you don't need to specify any policy attributes, specify an empty list \(`[]`\)\.  
*Required: *Yes  
*Type*: List of JSON name\-value pairs\.

`InstancePorts`  
A list of instance ports for the policy\. These are the ports associated with the back\-end server\.  
*Required: *No  
*Type*: List of String values

`LoadBalancerPorts`  
A list of external load balancer ports for the policy\.  
*Required*: Only for some policies\. For more information, see the *[Elastic Load Balancing Developer Guide](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/Welcome.html)*\.  
*Type*: List of String values

`PolicyName`  
A name for this policy that is unique to the load balancer\.  
*Required: *Yes  
*Type*: String

`PolicyType`  
The name of the policy type for this policy\. This must be one of the types reported by the Elastic Load Balancing [DescribeLoadBalancerPolicyTypes](http://docs.aws.amazon.com/ElasticLoadBalancing/latest/APIReference/API_DescribeLoadBalancerPolicyTypes.html) action\.  
*Required: *Yes  
*Type*: String

## Examples<a name="w3ab2c21c14d809b9"></a>

This example shows a snippet of the policies section of an elastic load balancer listener\.

```
"Policies" : [
   {
      "PolicyName" : "MySSLNegotiationPolicy",
      "PolicyType" : "SSLNegotiationPolicyType",
      "Attributes" : [
         { "Name" : "Protocol-TLSv1", "Value" : "true" },
         { "Name" : "Protocol-SSLv3", "Value" : "false" },
         { "Name" : "DHE-RSA-AES256-SHA", "Value" : "true" } ]
   }, {
      "PolicyName" : "MyAppCookieStickinessPolicy",
      "PolicyType" : "AppCookieStickinessPolicyType",
      "Attributes" : [
         { "Name" : "CookieName", "Value" : "MyCookie"} ]
   }, {
      "PolicyName" : "MyPublicKeyPolicy",
      "PolicyType" : "PublicKeyPolicyType",
      "Attributes" : [ {
         "Name" : "PublicKey",
         "Value" : { "Fn::Join" : [
            "\n", [
               "MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDh/51Aohx5VrpmlfGHZCzciMBa",
               "fkHve+MQYYJcxmNUKMdsWnz9WtVfKxxWUU7Cfor4lorYmENGCG8FWqCoLDMFs7pN",
               "yGEtpsrlKhzZWtgY1d7eGrUrBil03bI90E2KW0j4qAwGYAC8xixOkNClicojeEz4",
               "f4rr3sUf+ZBSsuMEuwIDAQAB" ]
         ] }
      } ]
   }, {
      "PolicyName" : "MyBackendServerAuthenticationPolicy",
      "PolicyType" : "BackendServerAuthenticationPolicyType",
      "Attributes" : [
         { "Name" : "PublicKeyPolicyName", "Value" : "MyPublicKeyPolicy" } ],
      "InstancePorts" : [ "8443" ]
   }
]
```

This example shows a snippet of the policies section of an elastic load balancer using proxy protocol\.

```
"Policies" : [{
   "PolicyName" : "EnableProxyProtocol",
   "PolicyType" : "ProxyProtocolPolicyType",
   "Attributes" : [{
      "Name"  : "ProxyProtocol",
      "Value" : "true"
   }],
   "InstancePorts" : [{"Ref" : "WebServerPort"}]
}]
```

In the following snippet, the load balancer uses a predefined security policy\. These predefined policies are provided by Elastic Load Balancing\. For more information, see [SSL Security Policies](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/elb-security-policy-options.html) in the *Elastic Load Balancing User Guide*\.

```
"Policies" : [{
   "PolicyName" : "ELBSecurityPolicyName",
   "PolicyType" : "SSLNegotiationPolicyType",
   "Attributes" : [{
      "Name"  : "Reference-Security-Policy",
      "Value" : "ELBSecurityPolicy-2014-10"
   }]
}]
```

## See Also<a name="w3ab2c21c14d809c11"></a>

+ 

+ 

+ 
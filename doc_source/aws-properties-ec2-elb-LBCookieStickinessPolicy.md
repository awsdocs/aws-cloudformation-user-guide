# ElasticLoadBalancing LBCookieStickinessPolicy Type<a name="aws-properties-ec2-elb-LBCookieStickinessPolicy"></a>

The LBCookieStickinessPolicy type is an embedded property of the AWS::ElasticLoadBalancing::LoadBalancer type\.

## Syntax<a name="w3ab2c21c14d801b5"></a>

### JSON<a name="aws-properties-ec2-elb-LBCookieStickinessPolicy-syntax.json"></a>

```
{
  "CookieExpirationPeriod" : String,
  "PolicyName" : String
}
```

### YAML<a name="aws-properties-ec2-elb-LBCookieStickinessPolicy-syntax.yaml"></a>

```
CookieExpirationPeriod: String
PolicyName: String
```

## Properties<a name="w3ab2c21c14d801b7"></a>

`CookieExpirationPeriod`  
The time period, in seconds, after which the cookie should be considered stale\. If this parameter isn't specified, the sticky session will last for the duration of the browser session\.  
*Required*: No  
*Type*: String

`PolicyName`  
The name of the policy being created\. The name must be unique within the set of policies for this load balancer\.  
To associate this policy with a listener, include the policy name in the listener's PolicyNames property\.

## See Also<a name="w3ab2c21c14d801b9"></a>

+ Sample template snippets in the Examples section of \.

+ [CreateLBCookieStickinessPolicy](http://docs.aws.amazon.com/ElasticLoadBalancing/latest/APIReference/API_CreateLBCookieStickinessPolicy.html) in the *Elastic Load Balancing API Reference version 2012\-06\-01*
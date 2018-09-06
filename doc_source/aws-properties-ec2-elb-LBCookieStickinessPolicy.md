# ElasticLoadBalancing LBCookieStickinessPolicy Type<a name="aws-properties-ec2-elb-LBCookieStickinessPolicy"></a>

The LBCookieStickinessPolicy type is an embedded property of the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) type\.

## Syntax<a name="w3ab2c21c14d988b5"></a>

### JSON<a name="aws-properties-ec2-elb-LBCookieStickinessPolicy-syntax.json"></a>

```
{
  "[CookieExpirationPeriod](#cfn-elb-lbcookiestickinesspolicy-cookieexpirationperiod)" : String,
  "[PolicyName](#cfn-elb-lbcookiestickinesspolicy-policyname)" : String
}
```

### YAML<a name="aws-properties-ec2-elb-LBCookieStickinessPolicy-syntax.yaml"></a>

```
[CookieExpirationPeriod](#cfn-elb-lbcookiestickinesspolicy-cookieexpirationperiod): String
[PolicyName](#cfn-elb-lbcookiestickinesspolicy-policyname): String
```

## Properties<a name="w3ab2c21c14d988b7"></a>

`CookieExpirationPeriod`  <a name="cfn-elb-lbcookiestickinesspolicy-cookieexpirationperiod"></a>
The time period, in seconds, after which the cookie should be considered stale\. If this parameter isn't specified, the sticky session will last for the duration of the browser session\.  
*Required*: No  
*Type*: String

`PolicyName`  <a name="cfn-elb-lbcookiestickinesspolicy-policyname"></a>
The name of the policy being created\. The name must be unique within the set of policies for this load balancer\.  
To associate this policy with a listener, include the policy name in the listener's [PolicyNames](aws-properties-ec2-elb-listener.md) property\.

## See Also<a name="w3ab2c21c14d988b9"></a>
+ Sample template snippets in the Examples section of [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)\.
+ [CreateLBCookieStickinessPolicy](http://docs.aws.amazon.com/ElasticLoadBalancing/latest/APIReference/API_CreateLBCookieStickinessPolicy.html) in the *Elastic Load Balancing API Reference version 2012\-06\-01*
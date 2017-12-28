# ElasticLoadBalancing AppCookieStickinessPolicy Type<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy"></a>

The AppCookieStickinessPolicy type is an embedded property of the AWS::ElasticLoadBalancing::LoadBalancer type\.

## Syntax<a name="w3ab2c21c14d783b5"></a>

### JSON<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy-syntax.json"></a>

```
{
   "CookieName" : String,
   "PolicyName" : String
}
```

### YAML<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy-syntax.yaml"></a>

```
CookieName: String
PolicyName: String
```

## Properties<a name="w3ab2c21c14d783b7"></a>

`CookieName`  
Name of the application cookie used for stickiness\.  
*Required*: Yes  
*Type*: String

`PolicyName`  
The name of the policy being created\. The name must be unique within the set of policies for this Load Balancer\.  
To associate this policy with a listener, include the policy name in the listener's PolicyNames property\.
*Required*: Yes  
*Type*: String

## See Also<a name="w3ab2c21c14d783b9"></a>

+ Sample template snippets in the Examples section of \.

+ [CreateAppCookieStickinessPolicy](http://docs.aws.amazon.com/ElasticLoadBalancing/latest/APIReference/API_CreateAppCookieStickinessPolicy.html)in the *Elastic Load Balancing API Reference version 2012\-06\-01*
# AWS::ElasticLoadBalancing::LoadBalancer AppCookieStickinessPolicy<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy"></a>

Specifies a policy for application\-controlled session stickiness for your Classic Load Balancer\.

To associate a policy with a listener, use the [PolicyNames](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb-listener.html#cfn-ec2-elb-listener-policynames) property for the listener\.

## Syntax<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy-syntax.json"></a>

```
{
  "[CookieName](#cfn-elb-appcookiestickinesspolicy-cookiename)" : String,
  "[PolicyName](#cfn-elb-appcookiestickinesspolicy-policyname)" : String
}
```

### YAML<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy-syntax.yaml"></a>

```
  [CookieName](#cfn-elb-appcookiestickinesspolicy-cookiename): String
  [PolicyName](#cfn-elb-appcookiestickinesspolicy-policyname): String
```

## Properties<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy-properties"></a>

`CookieName`  <a name="cfn-elb-appcookiestickinesspolicy-cookiename"></a>
The name of the application cookie used for stickiness\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-elb-appcookiestickinesspolicy-policyname"></a>
The mnemonic name for the policy being created\. The name must be unique within a set of policies for this load balancer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-elb-AppCookieStickinessPolicy--seealso"></a>
+  [CreateAppCookieStickinessPolicy](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_CreateAppCookieStickinessPolicy.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [Sticky Sessions](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-sticky-sessions.html) in the *User Guide for Classic Load Balancers* 


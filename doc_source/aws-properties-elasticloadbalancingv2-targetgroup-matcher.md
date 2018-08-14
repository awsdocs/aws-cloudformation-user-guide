# Elastic Load Balancing TargetGroup Matcher<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher"></a>

`Matcher` is a property of the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md) resource that specifies the HTTP codes that healthy targets must use when responding to an Elastic Load Balancing health check\.

## Syntax<a name="w3ab2c21c14e1028b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax.json"></a>

```
{
  "[HttpCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax.yaml"></a>

```
[HttpCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode): String
```

## Properties<a name="w3ab2c21c14e1028b7"></a>

`HttpCode`  <a name="cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode"></a>
The HTTP codes that a healthy target must use when responding to a health check, such as `200,202` or `200-399`\.   
For valid and default values, see the `HttpCode` contents for the [Matcher](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_Matcher.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: No  
*Type*: String
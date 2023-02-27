# AWS::ElasticLoadBalancingV2::TargetGroup Matcher<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher"></a>

Specifies the HTTP codes that healthy targets must use when responding to an HTTP health check\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax.json"></a>

```
{
  "[GrpcCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-grpccode)" : String,
  "[HttpCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax.yaml"></a>

```
  [GrpcCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-grpccode): String
  [HttpCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-properties"></a>

`GrpcCode`  <a name="cfn-elasticloadbalancingv2-targetgroup-matcher-grpccode"></a>
You can specify values between 0 and 99\. You can specify multiple values \(for example, "0,1"\) or a range of values \(for example, "0\-5"\)\. The default value is 12\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpCode`  <a name="cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode"></a>
For Application Load Balancers, you can specify values between 200 and 499, with the default value being 200\. You can specify multiple values \(for example, "200,202"\) or a range of values \(for example, "200\-299"\)\.  
For Network Load Balancers, you can specify values between 200 and 599, with the default value being 200\-399\. You can specify multiple values \(for example, "200,202"\) or a range of values \(for example, "200\-299"\)\.  
For Gateway Load Balancers, this must be "200–399"\.  
Note that when using shorthand syntax, some values such as commas need to be escaped\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
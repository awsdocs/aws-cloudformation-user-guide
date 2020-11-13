# AWS::ElasticLoadBalancingV2::TargetGroup Matcher<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher"></a>

Specifies the HTTP codes that healthy targets must use when responding to an HTTP health check\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax.json"></a>

```
{
  "[HttpCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode)" : String
  "[GrpcCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-grpccode)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-syntax.yaml"></a>

```
  [HttpCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode): String
  [GrpcCode](#cfn-elasticloadbalancingv2-targetgroup-matcher-grpccode): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-targetgroup-matcher-properties"></a>

`HttpCode`  <a name="cfn-elasticloadbalancingv2-targetgroup-matcher-httpcode"></a>
For Application Load Balancers, you can specify values between 200 and 499, and the default value is 200\. You can specify multiple values \(for example, "200,202"\) or a range of values \(for example, "200\-299"\)\. 

`GrpcCode` <a name="cfn-elasticloadbalancingv2-targetgroup-matcher-grpccode"></a> 
If the target group protocol is GRPC, you can specify value between 0 and 99, and the default value is 12\.You can specify multiple values (for example, "20,25") or a range of values (for example, "0-99").

*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

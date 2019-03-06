# Elastic Load Balancing V1 ConnectionDrainingPolicy<a name="aws-properties-ec2-elb-connectiondrainingpolicy"></a>

The `ConnectionDrainingPolicy` property describes how deregistered or unhealthy instances handle in\-flight requests for the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\. Connection draining ensures that the load balancer completes serving all in\-flight requests made to a registered instance when the instance is deregistered or becomes unhealthy\. Without connection draining, the load balancer closes connections to deregistered or unhealthy instances, and any in\-flight requests are not completed\.

For more information, see [Configure Connection Draining for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/config-conn-drain.html) in the *User Guide for Classic Load Balancers*\.

## Syntax<a name="w13ab1c21c10d135c16c25b7"></a>

### JSON<a name="aws-properties-ec2-elb-connectiondrainingpolicy-syntax.json"></a>

```
{
   "[Enabled](#cfn-elb-connectiondrainingpolicy-enabled)" : Boolean,
   "[Timeout](#cfn-elb-connectiondrainingpolicy-timeout)" : Integer
}
```

### YAML<a name="aws-properties-ec2-elb-connectiondrainingpolicy-syntax.yaml"></a>

```
[Enabled](#cfn-elb-connectiondrainingpolicy-enabled): Boolean
[Timeout](#cfn-elb-connectiondrainingpolicy-timeout): Integer
```

## Properties<a name="w13ab1c21c10d135c16c25b9"></a>

`Enabled`  <a name="cfn-elb-connectiondrainingpolicy-enabled"></a>
Indicates whether connection draining is enabled for the load balancer\.  
*Required*: Yes  
*Type*: Boolean

`Timeout`  <a name="cfn-elb-connectiondrainingpolicy-timeout"></a>
The maximum time, in seconds, to keep existing connections open before deregistering the instances\.  
*Required*: No  
*Type*: Integer
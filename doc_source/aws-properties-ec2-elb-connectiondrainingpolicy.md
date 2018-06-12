# Elastic Load Balancing ConnectionDrainingPolicy<a name="aws-properties-ec2-elb-connectiondrainingpolicy"></a>

The `ConnectionDrainingPolicy` property describes how deregistered or unhealthy instances handle in\-flight requests for the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\. Connection draining ensures that the load balancer completes serving all in\-flight requests made to a registered instance when the instance is deregistered or becomes unhealthy\. Without connection draining, the load balancer closes connections to deregistered or unhealthy instances, and any in\-flight requests are not completed\.

For more information about connection draining and default values, see [Enable or Disable Connection Draining for Your Load Balancer](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/config-conn-drain.html) in the *Elastic Load Balancing User Guide*\.

## Syntax<a name="w3ab2c21c14d974b7"></a>

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

## Properties<a name="w3ab2c21c14d974b9"></a>

`Enabled`  <a name="cfn-elb-connectiondrainingpolicy-enabled"></a>
Whether or not connection draining is enabled for the load balancer\.  
*Required*: Yes  
*Type*: Boolean

`Timeout`  <a name="cfn-elb-connectiondrainingpolicy-timeout"></a>
The time in seconds after the load balancer closes all connections to a deregistered or unhealthy instance\.  
*Required*: No  
*Type*: Integer
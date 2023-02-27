# AWS::ElasticLoadBalancingV2::TargetGroup TargetGroupAttribute<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattribute"></a>

Specifies a target group attribute\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattribute-syntax.json"></a>

```
{
  "[Key](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattribute-key)" : String,
  "[Value](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattribute-value)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattribute-syntax.yaml"></a>

```
  [Key](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattribute-key): String
  [Value](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattribute-value): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattribute-properties"></a>

`Key`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattribute-key"></a>
The name of the attribute\.  
The following attributes are supported by all load balancers:  
+  `deregistration_delay.timeout_seconds` \- The amount of time, in seconds, for Elastic Load Balancing to wait before changing the state of a deregistering target from `draining` to `unused`\. The range is 0\-3600 seconds\. The default value is 300 seconds\. If the target is a Lambda function, this attribute is not supported\.
+  `stickiness.enabled` \- Indicates whether target stickiness is enabled\. The value is `true` or `false`\. The default is `false`\.
+  `stickiness.type` \- Indicates the type of stickiness\. The possible values are:
  +  `lb_cookie` and `app_cookie` for Application Load Balancers\.
  +  `source_ip` for Network Load Balancers\.
  +  `source_ip_dest_ip` and `source_ip_dest_ip_proto` for Gateway Load Balancers\.
The following attributes are supported by Application Load Balancers and Network Load Balancers:  
+  `load_balancing.cross_zone.enabled` \- Indicates whether cross zone load balancing is enabled\. The value is `true`, `false` or `use_load_balancer_configuration`\. The default is `use_load_balancer_configuration`\.
+  `target_group_health.dns_failover.minimum_healthy_targets.count` \- The minimum number of targets that must be healthy\. If the number of healthy targets is below this value, mark the zone as unhealthy in DNS, so that traffic is routed only to healthy zones\. The possible values are `off` or an integer from 1 to the maximum number of targets\. The default is `off`\.
+  `target_group_health.dns_failover.minimum_healthy_targets.percentage` \- The minimum percentage of targets that must be healthy\. If the percentage of healthy targets is below this value, mark the zone as unhealthy in DNS, so that traffic is routed only to healthy zones\. The possible values are `off` or an integer from 1 to 100\. The default is `off`\.
+  `target_group_health.unhealthy_state_routing.minimum_healthy_targets.count` \- The minimum number of targets that must be healthy\. If the number of healthy targets is below this value, send traffic to all targets, including unhealthy targets\. The possible values are 1 to the maximum number of targets\. The default is 1\.
+  `target_group_health.unhealthy_state_routing.minimum_healthy_targets.percentage` \- The minimum percentage of targets that must be healthy\. If the percentage of healthy targets is below this value, send traffic to all targets, including unhealthy targets\. The possible values are `off` or an integer from 1 to 100\. The default is `off`\.
The following attributes are supported only if the load balancer is an Application Load Balancer and the target is an instance or an IP address:  
+  `load_balancing.algorithm.type` \- The load balancing algorithm determines how the load balancer selects targets when routing requests\. The value is `round_robin` or `least_outstanding_requests`\. The default is `round_robin`\.
+  `slow_start.duration_seconds` \- The time period, in seconds, during which a newly registered target receives an increasing share of the traffic to the target group\. After this time period ends, the target receives its full share of traffic\. The range is 30\-900 seconds \(15 minutes\)\. The default is 0 seconds \(disabled\)\.
+  `stickiness.app_cookie.cookie_name` \- Indicates the name of the application\-based cookie\. Names that start with the following prefixes are not allowed: `AWSALB`, `AWSALBAPP`, and `AWSALBTG`; they're reserved for use by the load balancer\.
+  `stickiness.app_cookie.duration_seconds` \- The time period, in seconds, during which requests from a client should be routed to the same target\. After this time period expires, the application\-based cookie is considered stale\. The range is 1 second to 1 week \(604800 seconds\)\. The default value is 1 day \(86400 seconds\)\.
+  `stickiness.lb_cookie.duration_seconds` \- The time period, in seconds, during which requests from a client should be routed to the same target\. After this time period expires, the load balancer\-generated cookie is considered stale\. The range is 1 second to 1 week \(604800 seconds\)\. The default value is 1 day \(86400 seconds\)\. 
The following attribute is supported only if the load balancer is an Application Load Balancer and the target is a Lambda function:  
+  `lambda.multi_value_headers.enabled` \- Indicates whether the request and response headers that are exchanged between the load balancer and the Lambda function include arrays of values or strings\. The value is `true` or `false`\. The default is `false`\. If the value is `false` and the request contains a duplicate header field name or query parameter key, the load balancer uses the last value sent by the client\.
The following attributes are supported only by Network Load Balancers:  
+  `deregistration_delay.connection_termination.enabled` \- Indicates whether the load balancer terminates connections at the end of the deregistration timeout\. The value is `true` or `false`\. The default is `false`\.
+  `preserve_client_ip.enabled` \- Indicates whether client IP preservation is enabled\. The value is `true` or `false`\. The default is disabled if the target group type is IP address and the target group protocol is TCP or TLS\. Otherwise, the default is enabled\. Client IP preservation cannot be disabled for UDP and TCP\_UDP target groups\.
+  `proxy_protocol_v2.enabled` \- Indicates whether Proxy Protocol version 2 is enabled\. The value is `true` or `false`\. The default is `false`\. 
The following attributes are supported only by Gateway Load Balancers:  
+  `target_failover.on_deregistration` \- Indicates how the Gateway Load Balancer handles existing flows when a target is deregistered\. The possible values are `rebalance` and `no_rebalance`\. The default is `no_rebalance`\. The two attributes \(`target_failover.on_deregistration` and `target_failover.on_unhealthy`\) can't be set independently\. The value you set for both attributes must be the same\. 
+  `target_failover.on_unhealthy` \- Indicates how the Gateway Load Balancer handles existing flows when a target is unhealthy\. The possible values are `rebalance` and `no_rebalance`\. The default is `no_rebalance`\. The two attributes \(`target_failover.on_deregistration` and `target_failover.on_unhealthy`\) cannot be set independently\. The value you set for both attributes must be the same\. 
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9._]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattribute-value"></a>
The value of the attribute\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
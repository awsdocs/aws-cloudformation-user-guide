# AWS::ElasticLoadBalancing::LoadBalancer HealthCheck<a name="aws-properties-ec2-elb-health-check"></a>

Specifies health check settings for your Classic Load Balancer\.

## Syntax<a name="aws-properties-ec2-elb-health-check-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-elb-health-check-syntax.json"></a>

```
{
  "[HealthyThreshold](#cfn-elb-healthcheck-healthythreshold)" : String,
  "[Interval](#cfn-elb-healthcheck-interval)" : String,
  "[Target](#cfn-elb-healthcheck-target)" : String,
  "[Timeout](#cfn-elb-healthcheck-timeout)" : String,
  "[UnhealthyThreshold](#cfn-elb-healthcheck-unhealthythreshold)" : String
}
```

### YAML<a name="aws-properties-ec2-elb-health-check-syntax.yaml"></a>

```
  [HealthyThreshold](#cfn-elb-healthcheck-healthythreshold): String
  [Interval](#cfn-elb-healthcheck-interval): String
  [Target](#cfn-elb-healthcheck-target): String
  [Timeout](#cfn-elb-healthcheck-timeout): String
  [UnhealthyThreshold](#cfn-elb-healthcheck-unhealthythreshold): String
```

## Properties<a name="aws-properties-ec2-elb-health-check-properties"></a>

`HealthyThreshold`  <a name="cfn-elb-healthcheck-healthythreshold"></a>
The number of consecutive health checks successes required before moving the instance to the `Healthy` state\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-elb-healthcheck-interval"></a>
The approximate interval, in seconds, between health checks of an individual instance\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-elb-healthcheck-target"></a>
The instance being checked\. The protocol is either TCP, HTTP, HTTPS, or SSL\. The range of valid ports is one \(1\) through 65535\.  
TCP is the default, specified as a TCP: port pair, for example "TCP:5000"\. In this case, a health check simply attempts to open a TCP connection to the instance on the specified port\. Failure to connect within the configured timeout is considered unhealthy\.  
SSL is also specified as SSL: port pair, for example, SSL:5000\.  
For HTTP/HTTPS, you must include a ping path in the string\. HTTP is specified as a HTTP:port;/;PathToPing; grouping, for example "HTTP:80/weather/us/wa/seattle"\. In this case, a HTTP GET request is issued to the instance on the given port and path\. Any answer other than "200 OK" within the timeout period is considered unhealthy\.  
The total length of the HTTP ping target must be 1024 16\-bit Unicode characters or less\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-elb-healthcheck-timeout"></a>
The amount of time, in seconds, during which no response means a failed health check\.  
This value must be less than the `Interval` value\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `60`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnhealthyThreshold`  <a name="cfn-elb-healthcheck-unhealthythreshold"></a>
The number of consecutive health check failures required before moving the instance to the `Unhealthy` state\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-elb-health-check--seealso"></a>
+  [ConfigureHealthCheck](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_ConfigureHealthCheck.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [Configure Health Checks](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-healthchecks.html) in the *User Guide for Classic Load Balancers* 


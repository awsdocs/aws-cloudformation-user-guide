# ElasticLoadBalancing LoadBalancer HealthCheck<a name="aws-properties-ec2-elb-health-check"></a>

The `HealthCheck` property configures health checks for the availability of your EC2 instances\. For more information, see [ Configure Health Checks for Your Classic Load Balancer](http://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-healthchecks.html) in the *User Guide for Classic Load Balancers*\.

`HealthCheck` is a property of the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource\.

## Syntax<a name="w3ab2c21c14d983b7"></a>

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

## Properties<a name="w3ab2c21c14d983b9"></a>

`HealthyThreshold`  <a name="cfn-elb-healthcheck-healthythreshold"></a>
Specifies the number of consecutive health probe successes required before moving the instance to the Healthy state\.  
*Required*: Yes  
*Type*: String

`Interval`  <a name="cfn-elb-healthcheck-interval"></a>
Specifies the approximate interval, in seconds, between health checks of an individual instance\. Valid values are `5` to `300`\. The default is `30`\.  
*Required*: Yes  
*Type*: String

`Target`  <a name="cfn-elb-healthcheck-target"></a>
Specifies the instance's protocol and port to check\. The protocol can be TCP, HTTP, HTTPS, or SSL\. The range of valid ports is 1 through 65535\.  
*Required*: Yes  
*Type*: String  
For TCP and SSL, you specify a port pair\. For example, you can specify `TCP:5000` or `SSL:5000`\. The health check attempts to open a TCP or SSL connection to the instance on the port that you specify\. If the health check fails to connect within the configured timeout period, the instance is considered unhealthy\.  
For HTTP or HTTPS, you specify a port and a path to ping \(`HTTP or HTTPS:port/PathToPing`\)\. For example, you can specify `HTTP:80/weather/us/wa/seattle`\. In this case, an HTTP GET request is issued to the instance on the given port and path\. If the health check receives any response other than `200 OK` within the configured timeout period, the instance is considered unhealthy\. The total length of the HTTP or HTTPS ping target cannot be more than 1024 16\-bit Unicode characters\.

`Timeout`  <a name="cfn-elb-healthcheck-timeout"></a>
Specifies the amount of time, in seconds, during which no response means a failed health probe\. This value must be less than the value for `Interval`\.  
*Required*: Yes  
*Type*: String

`UnhealthyThreshold`  <a name="cfn-elb-healthcheck-unhealthythreshold"></a>
Specifies the number of consecutive health probe failures required before moving the instance to the Unhealthy state\.  
*Required*: Yes  
*Type*: String
# Elastic Load Balancing ConnectionSettings<a name="aws-properties-ec2-elb-connectionsettings"></a>

`ConnectionSettings` is a property of the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource that describes how long the front\-end and back\-end connections of your load balancer can remain idle\. For more information, see [Configure Idle Connection Timeout](http://docs.aws.amazon.com/elasticloadbalancing/latest/classic/config-idle-timeout.html) in the *Elastic Load Balancing User Guide*\.

## Syntax<a name="w3ab2c21c14d978b5"></a>

### JSON<a name="aws-properties-ec2-elb-connectionsettings-syntax.json"></a>

```
{
  "[IdleTimeout](#cfn-elb-connectionsettings-idletimeout)" : Integer
}
```

### YAML<a name="aws-properties-ec2-elb-connectionsettings-syntax.yaml"></a>

```
[IdleTimeout](#cfn-elb-connectionsettings-idletimeout): Integer
```

## Properties<a name="w3ab2c21c14d978b7"></a>

`IdleTimeout`  <a name="cfn-elb-connectionsettings-idletimeout"></a>
The time \(in seconds\) that a connection to the load balancer can remain idle, which means no data is sent over the connection\. After the specified time, the load balancer closes the connection\.  
*Required*: Yes  
*Type*: Integer
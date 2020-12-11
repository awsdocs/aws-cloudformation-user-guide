# AWS::ElasticLoadBalancing::LoadBalancer ConnectionSettings<a name="aws-properties-ec2-elb-connectionsettings"></a>

Specifies the idle timeout value for your Classic Load Balancer\.

## Syntax<a name="aws-properties-ec2-elb-connectionsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-ec2-elb-connectionsettings-properties"></a>

`IdleTimeout`  <a name="cfn-elb-connectionsettings-idletimeout"></a>
The time, in seconds, that the connection is allowed to be idle \(no data has been sent over the connection\) before it is closed by the load balancer\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `3600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-elb-connectionsettings--seealso"></a>
+  [ModifyLoadBalancerAttributes](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_ModifyLoadBalancerAttributes.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [Idle Connection Timeout](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/config-idle-timeout.html) in the *User Guide for Classic Load Balancers* 


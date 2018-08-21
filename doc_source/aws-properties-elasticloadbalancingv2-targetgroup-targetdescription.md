# Elastic Load Balancing TargetGroup TargetDescription<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription"></a>

`TargetDescription` is a property of the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md) resource that specifies a target to add to an Elastic Load Balancing target group\.

## Syntax<a name="w3ab2c21c14e1032b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone)" : String,
  "[Id](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-id)" : String,
  "[Port](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-port)" : Integer
}
```

### YAML<a name="elasticloadbalancingv2-targetgroup-targetdescription"></a>

```
[AvailabilityZone](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone): String
[Id](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-id): String
[Port](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-port): Integer
```

## Properties<a name="w3ab2c21c14e1032b7"></a>

`AvailabilityZone`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone"></a>
The Availability Zone where the IP address is to be registered\. For more information, see [TargetDescription](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_TargetDescription.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: No  
*Type*: String

`Id`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetdescription-id"></a>
The ID of the target, such as an EC2 instance ID\. If the target type of the target group is `instance`, specify an instance ID\. If the target type is `ip`, specify an IP address\.  
*Required*: Yes  
*Type*: String

`Port`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetdescription-port"></a>
The port number on which the target is listening for traffic\.  
*Required*: No  
*Type*: Integer
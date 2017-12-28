# Elastic Load Balancing TargetGroup TargetDescription<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription"></a>

`TargetDescription` is a property of the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md) resource that specifies a target to add to an Elastic Load Balancing target group\.

## Syntax<a name="w3ab2c21c14d845b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-port)" : Integer
}
```

### YAML<a name="elasticloadbalancingv2-targetgroup-targetdescription"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-port): Integer
```

## Properties<a name="w3ab2c21c14d845b7"></a>

`AvailabilityZone`  
The Availability Zone where the IP address is to be registered\. For more information, see [TargetDescription](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_TargetDescription.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *No  
*Type*: String

`Id`  
The ID of the target, such as an EC2 instance ID\. If the target type of the target group is `instance`, specify an instance ID\. If the target type is `ip`, specify an IP address\.  
*Required: *Yes  
*Type*: String

`Port`  
The port number on which the target is listening for traffic\.  
*Required: *No  
*Type*: Integer
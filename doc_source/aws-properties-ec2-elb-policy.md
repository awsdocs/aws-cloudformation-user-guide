# AWS::ElasticLoadBalancing::LoadBalancer Policies<a name="aws-properties-ec2-elb-policy"></a>

Specifies policies for your Classic Load Balancer\.

To associate policies with a listener, use the [PolicyNames](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb-listener.html#cfn-ec2-elb-listener-policynames) property for the listener\.

## Syntax<a name="aws-properties-ec2-elb-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-elb-policy-syntax.json"></a>

```
{
  "[Attributes](#cfn-ec2-elb-policy-attributes)" : [ Json, ... ],
  "[InstancePorts](#cfn-ec2-elb-policy-instanceports)" : [ String, ... ],
  "[LoadBalancerPorts](#cfn-ec2-elb-policy-loadbalancerports)" : [ String, ... ],
  "[PolicyName](#cfn-ec2-elb-policy-policyname)" : String,
  "[PolicyType](#cfn-ec2-elb-policy-policytype)" : String
}
```

### YAML<a name="aws-properties-ec2-elb-policy-syntax.yaml"></a>

```
  [Attributes](#cfn-ec2-elb-policy-attributes): 
    - Json
  [InstancePorts](#cfn-ec2-elb-policy-instanceports): 
    - String
  [LoadBalancerPorts](#cfn-ec2-elb-policy-loadbalancerports): 
    - String
  [PolicyName](#cfn-ec2-elb-policy-policyname): String
  [PolicyType](#cfn-ec2-elb-policy-policytype): String
```

## Properties<a name="aws-properties-ec2-elb-policy-properties"></a>

`Attributes`  <a name="cfn-ec2-elb-policy-attributes"></a>
The policy attributes\.  
*Required*: Yes  
*Type*: List of Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstancePorts`  <a name="cfn-ec2-elb-policy-instanceports"></a>
The instance ports for the policy\. Required only for some policy types\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerPorts`  <a name="cfn-ec2-elb-policy-loadbalancerports"></a>
The load balancer ports for the policy\. Required only for some policy types\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-ec2-elb-policy-policyname"></a>
The name of the policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-ec2-elb-policy-policytype"></a>
The name of the policy type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ec2-elb-policy--examples"></a>

### <a name="aws-properties-ec2-elb-policy--examples--"></a>

#### JSON<a name="aws-properties-ec2-elb-policy--examples----json"></a>

```
"Policies": [{
    "PolicyName": "My-SSLNegotiation-Policy",
    "PolicyType": "SSLNegotiationPolicyType",
    "Attributes": [{
        "Name": "Reference-Security-Policy",
        "Value": "ELBSecurityPolicy-TLS-1-2-2017-01"
    }]
}]
```

#### YAML<a name="aws-properties-ec2-elb-policy--examples----yaml"></a>

```
Policies:
    - PolicyName: My-SSLNegotiation-Policy
      PolicyType: SSLNegotiationPolicyType
      Attributes:
      - Name: Reference-Security-Policy
        Value: ELBSecurityPolicy-TLS-1-2-2017-01
```

## See also<a name="aws-properties-ec2-elb-policy--seealso"></a>
+  [CreateLoadBalancerPolicy](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_CreateLoadBalancerPolicy.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 


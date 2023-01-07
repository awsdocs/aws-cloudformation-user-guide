# AWS::EC2::NetworkInsightsAnalysis AnalysisLoadBalancerListener<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancerlistener"></a>

Describes a load balancer listener\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancerlistener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancerlistener-syntax.json"></a>

```
{
  "[InstancePort](#cfn-ec2-networkinsightsanalysis-analysisloadbalancerlistener-instanceport)" : Integer,
  "[LoadBalancerPort](#cfn-ec2-networkinsightsanalysis-analysisloadbalancerlistener-loadbalancerport)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancerlistener-syntax.yaml"></a>

```
  [InstancePort](#cfn-ec2-networkinsightsanalysis-analysisloadbalancerlistener-instanceport): Integer
  [LoadBalancerPort](#cfn-ec2-networkinsightsanalysis-analysisloadbalancerlistener-loadbalancerport): Integer
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancerlistener-properties"></a>

`InstancePort`  <a name="cfn-ec2-networkinsightsanalysis-analysisloadbalancerlistener-instanceport"></a>
\[Classic Load Balancers\] The back\-end port for the listener\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerPort`  <a name="cfn-ec2-networkinsightsanalysis-analysisloadbalancerlistener-loadbalancerport"></a>
The port on which the load balancer is listening\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
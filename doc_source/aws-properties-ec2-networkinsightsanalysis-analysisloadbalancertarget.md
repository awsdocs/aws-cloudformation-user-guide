# AWS::EC2::NetworkInsightsAnalysis AnalysisLoadBalancerTarget<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancertarget"></a>

Describes a load balancer target\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancertarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancertarget-syntax.json"></a>

```
{
  "[Address](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-address)" : String,
  "[AvailabilityZone](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-availabilityzone)" : String,
  "[Instance](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-instance)" : AnalysisComponent,
  "[Port](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-port)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancertarget-syntax.yaml"></a>

```
  [Address](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-address): String
  [AvailabilityZone](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-availabilityzone): String
  [Instance](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-instance): 
    AnalysisComponent
  [Port](#cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-port): Integer
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-analysisloadbalancertarget-properties"></a>

`Address`  <a name="cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-address"></a>
The IP address\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `15`  
*Pattern*: `^([0-9]{1,3}.){3}[0-9]{1,3}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-availabilityzone"></a>
The Availability Zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Instance`  <a name="cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-instance"></a>
Information about the instance\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-ec2-networkinsightsanalysis-analysisloadbalancertarget-port"></a>
The port on which the target is listening\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::EC2::TrafficMirrorFilterRule TrafficMirrorPortRange<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrange"></a>

Describes the Traffic Mirror port range\.

## Syntax<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrange-syntax.json"></a>

```
{
  "[FromPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrange-fromport)" : Integer,
  "[ToPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrange-toport)" : Integer
}
```

### YAML<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrange-syntax.yaml"></a>

```
  [FromPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrange-fromport): Integer
  [ToPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrange-toport): Integer
```

## Properties<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrange-properties"></a>

`FromPort`  <a name="cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrange-fromport"></a>
The start of the Traffic Mirror port range\. This applies to the TCP and UDP protocols\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrange-toport"></a>
The end of the Traffic Mirror port range\. This applies to the TCP and UDP protocols\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
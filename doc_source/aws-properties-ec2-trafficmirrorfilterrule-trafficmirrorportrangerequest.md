# AWS::EC2::TrafficMirrorFilterRule TrafficMirrorPortRangeRequest<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest"></a>

Information about the Traffic Mirror filter rule port range\.

## Syntax<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-syntax.json"></a>

```
{
  "[FromPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-fromport)" : Integer,
  "[ToPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-toport)" : Integer
}
```

### YAML<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-syntax.yaml"></a>

```
  [FromPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-fromport): Integer
  [ToPort](#cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-toport): Integer
```

## Properties<a name="aws-properties-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-properties"></a>

`FromPort`  <a name="cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-fromport"></a>
The first port in the Traffic Mirror port range\. This applies to the TCP and UDP protocols\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-ec2-trafficmirrorfilterrule-trafficmirrorportrangerequest-toport"></a>
The last port in the Traffic Mirror port range\. This applies to the TCP and UDP protocols\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
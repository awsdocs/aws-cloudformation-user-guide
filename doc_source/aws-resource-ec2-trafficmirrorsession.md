# AWS::EC2::TrafficMirrorSession<a name="aws-resource-ec2-trafficmirrorsession"></a>

Creates a Traffic Mirror session\.

A Traffic Mirror session actively copies packets from a Traffic Mirror source to a Traffic Mirror target\. Create a filter, and then assign it to the session to define a subset of the traffic to mirror, for example all TCP traffic\.

The Traffic Mirror source and the Traffic Mirror target \(monitoring appliances\) can be in the same VPC, or in a different VPC connected via VPC peering or a transit gateway\. 

By default, no traffic is mirrored\. Use [AWS::EC2::TrafficMirrorFilterRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrorfilterrule.html) to specify filter rules that specify the traffic to mirror\.

## Syntax<a name="aws-resource-ec2-trafficmirrorsession-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-trafficmirrorsession-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TrafficMirrorSession",
  "Properties" : {
      "[Description](#cfn-ec2-trafficmirrorsession-description)" : String,
      "[NetworkInterfaceId](#cfn-ec2-trafficmirrorsession-networkinterfaceid)" : String,
      "[PacketLength](#cfn-ec2-trafficmirrorsession-packetlength)" : Integer,
      "[SessionNumber](#cfn-ec2-trafficmirrorsession-sessionnumber)" : Integer,
      "[Tags](#cfn-ec2-trafficmirrorsession-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TrafficMirrorFilterId](#cfn-ec2-trafficmirrorsession-trafficmirrorfilterid)" : String,
      "[TrafficMirrorTargetId](#cfn-ec2-trafficmirrorsession-trafficmirrortargetid)" : String,
      "[VirtualNetworkId](#cfn-ec2-trafficmirrorsession-virtualnetworkid)" : Integer
    }
}
```

### YAML<a name="aws-resource-ec2-trafficmirrorsession-syntax.yaml"></a>

```
Type: AWS::EC2::TrafficMirrorSession
Properties: 
  [Description](#cfn-ec2-trafficmirrorsession-description): String
  [NetworkInterfaceId](#cfn-ec2-trafficmirrorsession-networkinterfaceid): String
  [PacketLength](#cfn-ec2-trafficmirrorsession-packetlength): Integer
  [SessionNumber](#cfn-ec2-trafficmirrorsession-sessionnumber): Integer
  [Tags](#cfn-ec2-trafficmirrorsession-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TrafficMirrorFilterId](#cfn-ec2-trafficmirrorsession-trafficmirrorfilterid): String
  [TrafficMirrorTargetId](#cfn-ec2-trafficmirrorsession-trafficmirrortargetid): String
  [VirtualNetworkId](#cfn-ec2-trafficmirrorsession-virtualnetworkid): Integer
```

## Properties<a name="aws-resource-ec2-trafficmirrorsession-properties"></a>

`Description`  <a name="cfn-ec2-trafficmirrorsession-description"></a>
The description of the Traffic Mirror session\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-trafficmirrorsession-networkinterfaceid"></a>
The ID of the source network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PacketLength`  <a name="cfn-ec2-trafficmirrorsession-packetlength"></a>
The number of bytes in each packet to mirror\. These are bytes after the VXLAN header\. Do not specify this parameter when you want to mirror the entire packet\. To mirror a subset of the packet, set this to the length \(in bytes\) that you want to mirror\. For example, if you set this value to 100, then the first 100 bytes that meet the filter criteria are copied to the target\.  
If you do not want to mirror the entire packet, use the `PacketLength` parameter to specify the number of bytes in each packet to mirror\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionNumber`  <a name="cfn-ec2-trafficmirrorsession-sessionnumber"></a>
The session number determines the order in which sessions are evaluated when an interface is used by multiple sessions\. The first session with a matching filter is the one that mirrors the packets\.  
Valid values are 1\-32766\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-trafficmirrorsession-tags"></a>
The tags to assign to a Traffic Mirror session\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficMirrorFilterId`  <a name="cfn-ec2-trafficmirrorsession-trafficmirrorfilterid"></a>
The ID of the Traffic Mirror filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficMirrorTargetId`  <a name="cfn-ec2-trafficmirrorsession-trafficmirrortargetid"></a>
The ID of the Traffic Mirror target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualNetworkId`  <a name="cfn-ec2-trafficmirrorsession-virtualnetworkid"></a>
The VXLAN ID for the Traffic Mirror session\. For more information about the VXLAN protocol, see [RFC 7348](https://tools.ietf.org/html/rfc7348)\. If you do not specify a `VirtualNetworkId`, an account\-wide unique id is chosen at random\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-trafficmirrorsession-return-values"></a>

### Ref<a name="aws-resource-ec2-trafficmirrorsession-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Traffic Mirror Session\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-trafficmirrorsession--examples"></a>

### Create a Traffic Mirror Session<a name="aws-resource-ec2-trafficmirrorsession--examples--Create_a_Traffic_Mirror_Session"></a>

This is a traffic mirror session that mirrors the first 100 bytes in each packet\.

#### JSON<a name="aws-resource-ec2-trafficmirrorsession--examples--Create_a_Traffic_Mirror_Session--json"></a>

```
{
  "SampleTrafficMirrorSession": {
    "Type": "AWS::EC2::TrafficMirrorSession",
    "Properties": {
      "Description": "Example traffic mirror session",
      "NetworkInterfaceId": "eni-070203a001EXAMPLE",
      "TrafficMirrorTargetId": "tmt-5319fsEXAMPLE",
      "TrafficMirrorFilterId": "tmf-1tdbhqEXAMPLE",
      "SessionNumber": 1,
      "PacketLength": 100,
      "VirtualNetworkId": 1234,
      "Tags": [
        {
          "Key": "Name",
          "Value": "SampleSession"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-trafficmirrorsession--examples--Create_a_Traffic_Mirror_Session--yaml"></a>

```
SampleTrafficMirrorSession:
  Type: "AWS::EC2::TrafficMirrorSession"
  Properties:
    Description: "Example traffic mirror session"
    NetworkInterfaceId: "eni-070203a001EXAMPLE"
    TrafficMirrorTargetId: "tmt-5319fsEXAMPLE"
    TrafficMirrorFilterId: "tmf-1tdbhqEXAMPLE"
    SessionNumber: 1
    PacketLength: 100
    VirtualNetworkId: 1234
    Tags:
    - Key: "Name"
      Value: "SampleSession"
```

## See also<a name="aws-resource-ec2-trafficmirrorsession--seealso"></a>
+ [Traffic Mirror Sessions](https://docs.aws.amazon.com/vpc/latest/mirroring/traffic-mirroring-how-it-works.html#traffic-mirroring-sessions) in *Traffic Mirroring*
+ [CreateTrafficMirrorSession](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTrafficMirrorSession.html) in the *Amazon EC2 API Reference*


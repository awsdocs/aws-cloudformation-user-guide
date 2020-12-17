# AWS::EC2::TrafficMirrorTarget<a name="aws-resource-ec2-trafficmirrortarget"></a>

Specifies a target for your Traffic Mirror session\.

A Traffic Mirror target is the destination for mirrored traffic\. The Traffic Mirror source and the Traffic Mirror target \(monitoring appliances\) can be in the same VPC, or in different VPCs connected via VPC peering or a transit gateway\.

A Traffic Mirror target can be a network interface, or a Network Load Balancer\.

To use the target in a Traffic Mirror session, use [AWS::EC2::TrafficMirrorSession](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrorsession.html)\.

## Syntax<a name="aws-resource-ec2-trafficmirrortarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-trafficmirrortarget-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TrafficMirrorTarget",
  "Properties" : {
      "[Description](#cfn-ec2-trafficmirrortarget-description)" : String,
      "[NetworkInterfaceId](#cfn-ec2-trafficmirrortarget-networkinterfaceid)" : String,
      "[NetworkLoadBalancerArn](#cfn-ec2-trafficmirrortarget-networkloadbalancerarn)" : String,
      "[Tags](#cfn-ec2-trafficmirrortarget-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-trafficmirrortarget-syntax.yaml"></a>

```
Type: AWS::EC2::TrafficMirrorTarget
Properties: 
  [Description](#cfn-ec2-trafficmirrortarget-description): String
  [NetworkInterfaceId](#cfn-ec2-trafficmirrortarget-networkinterfaceid): String
  [NetworkLoadBalancerArn](#cfn-ec2-trafficmirrortarget-networkloadbalancerarn): String
  [Tags](#cfn-ec2-trafficmirrortarget-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-trafficmirrortarget-properties"></a>

`Description`  <a name="cfn-ec2-trafficmirrortarget-description"></a>
The description of the Traffic Mirror target\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaceId`  <a name="cfn-ec2-trafficmirrortarget-networkinterfaceid"></a>
The network interface ID that is associated with the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkLoadBalancerArn`  <a name="cfn-ec2-trafficmirrortarget-networkloadbalancerarn"></a>
The Amazon Resource Name \(ARN\) of the Network Load Balancer that is associated with the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-trafficmirrortarget-tags"></a>
The tags to assign to the Traffic Mirror target\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-trafficmirrortarget-return-values"></a>

### Ref<a name="aws-resource-ec2-trafficmirrortarget-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Traffic Mirror target\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-trafficmirrortarget--examples"></a>

### Create a Traffic Mirror Target Associated with a Network Load Balancer<a name="aws-resource-ec2-trafficmirrortarget--examples--Create_a_Traffic_Mirror_Target_Associated_with_a_Network_Load_Balancer"></a>

This is a traffic mirror target associated with a network load balancer\.

#### JSON<a name="aws-resource-ec2-trafficmirrortarget--examples--Create_a_Traffic_Mirror_Target_Associated_with_a_Network_Load_Balancer--json"></a>

```
{
  "SampleNLBTrafficMirrorTarget": {
    "Type": "AWS::EC2::TrafficMirrorTarget",
    "Properties": {
      "Description": "Example traffic mirror target associated with a network load balancer",
      "NetworkLoadBalancerArn": "arn:aws:elasticloadbalancing:us-east-1:724145273726:loadbalancer/net/NLB/7cabvhEXAMPLE",
       "Tags": [
        {
          "Key": "Name",
          "Value": "SampleNLBTarget"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-trafficmirrortarget--examples--Create_a_Traffic_Mirror_Target_Associated_with_a_Network_Load_Balancer--yaml"></a>

```
SampleNLBTrafficMirrorTarget:
  Type: "AWS::EC2::TrafficMirrorTarget"
  Properties:
    Description: "Example traffic mirror target associated with a network load balancer",
    NetworkLoadBalancerArn: "arn:aws:elasticloadbalancing:us-east-1:724145273726:loadbalancer/net/NLB/7cabvhEXAMPLE"
  Tags:
    - Key: "Name"
      Value: "SampleNLBTarget"
```

### Create a Traffic Mirror Target Associated with a Network Interface<a name="aws-resource-ec2-trafficmirrortarget--examples--Create_a_Traffic_Mirror_Target_Associated_with_a_Network_Interface"></a>

This is a traffic mirror target associated with a network interface\.

#### JSON<a name="aws-resource-ec2-trafficmirrortarget--examples--Create_a_Traffic_Mirror_Target_Associated_with_a_Network_Interface--json"></a>

```
{
  "SampleNetworkInterfaceTarget": {
    "Type": "AWS::EC2::TrafficMirrorTarget",
    "Properties": {
      "Description": "Example traffic mirror target associated with a network interface",
      "NetworkInterfaceId": "eni-070203a001EXAMPLE",
      "Tags": [
        {
          "Key": "Name",
          "Value": "SampleNetworkInterfaceTarget"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-trafficmirrortarget--examples--Create_a_Traffic_Mirror_Target_Associated_with_a_Network_Interface--yaml"></a>

```
SampleNetworkInterfaceTarget:
  Type: "AWS::EC2::TrafficMirrorTarget"
  Properties:
    Description: "Example traffic mirror target associated with a network interface"
    NetworkInterfaceId: "eni-070203a001EXAMPLE"
    Tags:
    - Key: "Name"
      Value: "SampleNetworkInterfaceTarget"
```

## See also<a name="aws-resource-ec2-trafficmirrortarget--seealso"></a>
+ [Traffic Mirror Targets](https://docs.aws.amazon.com/vpc/latest/mirroring/traffic-mirroring-how-it-works.html#traffic-mirroring-targets) in *Traffic Mirroring*
+ [CreateTrafficMirrorTarget](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTrafficMirrorTarget.html) in the *Amazon EC2 API Reference*


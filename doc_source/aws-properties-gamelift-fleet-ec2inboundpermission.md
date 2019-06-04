# AWS::GameLift::Fleet IpPermission<a name="aws-properties-gamelift-fleet-ec2inboundpermission"></a>

A range of IP addresses and port settings that allow inbound traffic to connect to server processes on Amazon GameLift\. Each game session hosted on a fleet is assigned a unique combination of IP address and port number, which must fall into the fleet's allowed ranges\. For fleets created with a custom game server, the ranges reflect the server's game session assignments\. For Realtime Servers fleets, Amazon GameLift automatically opens two port ranges, one for TCP messaging and one for UDP for use by the Realtime servers\. 

## Syntax<a name="aws-properties-gamelift-fleet-ec2inboundpermission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-ec2inboundpermission-syntax.json"></a>

```
{
  "[FromPort](#cfn-gamelift-fleet-ec2inboundpermissions-fromport)" : Integer,
  "[IpRange](#cfn-gamelift-fleet-ec2inboundpermissions-iprange)" : String,
  "[Protocol](#cfn-gamelift-fleet-ec2inboundpermissions-protocol)" : String,
  "[ToPort](#cfn-gamelift-fleet-ec2inboundpermissions-toport)" : Integer
}
```

### YAML<a name="aws-properties-gamelift-fleet-ec2inboundpermission-syntax.yaml"></a>

```
  [FromPort](#cfn-gamelift-fleet-ec2inboundpermissions-fromport): Integer
  [IpRange](#cfn-gamelift-fleet-ec2inboundpermissions-iprange): String
  [Protocol](#cfn-gamelift-fleet-ec2inboundpermissions-protocol): String
  [ToPort](#cfn-gamelift-fleet-ec2inboundpermissions-toport): Integer
```

## Properties<a name="aws-properties-gamelift-fleet-ec2inboundpermission-properties"></a>

`FromPort`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-fromport"></a>
Starting value for a range of allowed port numbers\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `60000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpRange`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-iprange"></a>
Range of allowed IP addresses\. This value must be expressed in CIDR notation\. Example: "`000.000.000.000/[subnet mask]`" or optionally the shortened version "`0.0.0.0/[subnet mask]`"\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[^\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-protocol"></a>
Network communication protocol used by the fleet\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `TCP | UDP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-toport"></a>
Ending value for a range of allowed port numbers\. Port numbers are end\-inclusive\. This value must be higher than `FromPort`\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `60000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-gamelift-fleet-ec2inboundpermission--seealso"></a>
+  [IpPermission](https://docs.aws.amazon.com/gamelift/latest/apireference/API_IpPermission.html) in the *Amazon GameLift API Reference* 
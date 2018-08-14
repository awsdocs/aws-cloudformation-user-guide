# Amazon GameLift Fleet EC2InboundPermission<a name="aws-properties-gamelift-fleet-ec2inboundpermission"></a>

`EC2InboundPermission` is a property of the [AWS::GameLift::Fleet](aws-resource-gamelift-fleet.md) resource that specifies the traffic that is permitted to access your game servers in an Amazon GameLift \(GameLift\) fleet\.

## Syntax<a name="w3ab2c21c14e1217b5"></a>

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

## Properties<a name="w3ab2c21c14e1217b7"></a>

`FromPort`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-fromport"></a>
The starting value for a range of allowed port numbers\. This value must be lower than the `ToPort` value\.  
*Required*: Yes  
*Type*: Integer

`IpRange`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-iprange"></a>
The range of allowed IP addresses in CIDR notation\.  
*Required*: Yes  
*Type*: String

`Protocol`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-protocol"></a>
The network communication protocol that is used by the fleet\. For valid values, see the [IpPermission](http://docs.aws.amazon.com/gamelift/latest/apireference/API_IpPermission.html) data type in the *Amazon GameLift API Reference*\.  
*Required*: Yes  
*Type*: String

`ToPort`  <a name="cfn-gamelift-fleet-ec2inboundpermissions-toport"></a>
The ending value for a range of allowed port numbers\. This value must be higher than the `FromPort` value\.   
*Required*: Yes  
*Type*: Integer
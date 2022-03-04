# AWS::GameLift::Fleet IpPermission<a name="aws-properties-gamelift-fleet-ippermission"></a>

A range of IP addresses and port settings that allow inbound traffic to connect to server processes on an instance in a fleet\. New game sessions are assigned an IP address/port number combination, which must fall into the fleet's allowed ranges\. Fleets with custom game builds must have permissions explicitly set\. For Realtime Servers fleets, GameLift automatically opens two port ranges, one for TCP messaging and one for UDP\.

## Syntax<a name="aws-properties-gamelift-fleet-ippermission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-ippermission-syntax.json"></a>

```
{
  "[FromPort](#cfn-gamelift-fleet-ippermission-fromport)" : Integer,
  "[IpRange](#cfn-gamelift-fleet-ippermission-iprange)" : String,
  "[Protocol](#cfn-gamelift-fleet-ippermission-protocol)" : String,
  "[ToPort](#cfn-gamelift-fleet-ippermission-toport)" : Integer
}
```

### YAML<a name="aws-properties-gamelift-fleet-ippermission-syntax.yaml"></a>

```
  [FromPort](#cfn-gamelift-fleet-ippermission-fromport): Integer
  [IpRange](#cfn-gamelift-fleet-ippermission-iprange): String
  [Protocol](#cfn-gamelift-fleet-ippermission-protocol): String
  [ToPort](#cfn-gamelift-fleet-ippermission-toport): Integer
```

## Properties<a name="aws-properties-gamelift-fleet-ippermission-properties"></a>

`FromPort`  <a name="cfn-gamelift-fleet-ippermission-fromport"></a>
A starting value for a range of allowed port numbers\.  
For fleets using Windows and Linux builds, only ports 1026\-60000 are valid\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `60000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpRange`  <a name="cfn-gamelift-fleet-ippermission-iprange"></a>
A range of allowed IP addresses\. This value must be expressed in CIDR notation\. Example: "`000.000.000.000/[subnet mask]`" or optionally the shortened version "`0.0.0.0/[subnet mask]`"\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[^\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-gamelift-fleet-ippermission-protocol"></a>
The network communication protocol used by the fleet\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `TCP | UDP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-gamelift-fleet-ippermission-toport"></a>
An ending value for a range of allowed port numbers\. Port numbers are end\-inclusive\. This value must be higher than `FromPort`\.  
For fleets using Windows and Linux builds, only ports 1026\-60000 are valid\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `60000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-fleet-ippermission--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift fleet for a custom game build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [IpPermission](https://docs.aws.amazon.com/gamelift/latest/apireference/API_IpPermission.html) in the *Amazon GameLift API Reference* 


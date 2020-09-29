# AWS::GameLift::GameServerGroup VpcSubnets<a name="aws-properties-gamelift-gameservergroup-vpcsubnets"></a>

A list of virtual private cloud \(VPC\) subnets to use with instances in the game server group\. By default, all GameLift FleetIQ\-supported Availability Zones are used\. You can use this parameter to specify VPCs that you've set up\. This property cannot be updated after the game server group is created, and the corresponding Auto Scaling group will always use the property value that is set with this request, even if the Auto Scaling group is updated directly\.

## Syntax<a name="aws-properties-gamelift-gameservergroup-vpcsubnets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gameservergroup-vpcsubnets-syntax.json"></a>

```
{
  "[VpcSubnets](#cfn-gamelift-gameservergroup-vpcsubnets-vpcsubnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-gamelift-gameservergroup-vpcsubnets-syntax.yaml"></a>

```
  [VpcSubnets](#cfn-gamelift-gameservergroup-vpcsubnets-vpcsubnets): 
    - String
```

## Properties<a name="aws-properties-gamelift-gameservergroup-vpcsubnets-properties"></a>

`VpcSubnets`  <a name="cfn-gamelift-gameservergroup-vpcsubnets-vpcsubnets"></a>
A list of virtual private cloud \(VPC\) subnets to use with instances in the game server group\. By default, all GameLift FleetIQ\-supported Availability Zones are used\. You can use this parameter to specify VPCs that you've set up\. This property cannot be updated after the game server group is created, and the corresponding Auto Scaling group will always use the property value that is set with this request, even if the Auto Scaling group is updated directly\.  
*Required*: No  
*Type*: [List](#aws-properties-gamelift-gameservergroup-vpcsubnets) of [String](#aws-properties-gamelift-gameservergroup-vpcsubnets)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-gameservergroup-vpcsubnets--seealso"></a>
+  [GameLift FleetIQ Guide](https://docs.aws.amazon.com/gamelift/latest/developerguide/gsg-intro.html) 
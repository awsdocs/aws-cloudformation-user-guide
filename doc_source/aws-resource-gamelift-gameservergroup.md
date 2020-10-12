# AWS::GameLift::GameServerGroup<a name="aws-resource-gamelift-gameservergroup"></a>

The `AWS::GameLift::GameServerGroup` resource creates a GameLift FleetIQ game server group for managing game hosting on a collection of Amazon EC2 instances\. This operation creates the game server group and also creates an associated EC2 Auto Scaling group in your AWS account\. After the groups are created, some properties can be viewed and updated in the GameLift FleetIQ game server group, while others are managed directly in the Auto Scaling group\. GameLift FleetIQ, as part of its balancing activities to optimize the group's instances for low\-cost game hosting, routinely updates certain Auto Scaling group properties\. Game server group metrics and events are emitted to Amazon CloudWatch\.

## Syntax<a name="aws-resource-gamelift-gameservergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-gameservergroup-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::GameServerGroup",
  "Properties" : {
      "[AutoScalingPolicy](#cfn-gamelift-gameservergroup-autoscalingpolicy)" : AutoScalingPolicy,
      "[BalancingStrategy](#cfn-gamelift-gameservergroup-balancingstrategy)" : String,
      "[DeleteOption](#cfn-gamelift-gameservergroup-deleteoption)" : String,
      "[GameServerGroupName](#cfn-gamelift-gameservergroup-gameservergroupname)" : String,
      "[GameServerProtectionPolicy](#cfn-gamelift-gameservergroup-gameserverprotectionpolicy)" : String,
      "[InstanceDefinitions](#cfn-gamelift-gameservergroup-instancedefinitions)" : InstanceDefinitions,
      "[LaunchTemplate](#cfn-gamelift-gameservergroup-launchtemplate)" : LaunchTemplate,
      "[MaxSize](#cfn-gamelift-gameservergroup-maxsize)" : Double,
      "[MinSize](#cfn-gamelift-gameservergroup-minsize)" : Double,
      "[RoleArn](#cfn-gamelift-gameservergroup-rolearn)" : String,
      "[Tags](#cfn-gamelift-gameservergroup-tags)" : Tags,
      "[VpcSubnets](#cfn-gamelift-gameservergroup-vpcsubnets)" : VpcSubnets
    }
}
```

### YAML<a name="aws-resource-gamelift-gameservergroup-syntax.yaml"></a>

```
Type: AWS::GameLift::GameServerGroup
Properties: 
  [AutoScalingPolicy](#cfn-gamelift-gameservergroup-autoscalingpolicy): 
    AutoScalingPolicy
  [BalancingStrategy](#cfn-gamelift-gameservergroup-balancingstrategy): String
  [DeleteOption](#cfn-gamelift-gameservergroup-deleteoption): String
  [GameServerGroupName](#cfn-gamelift-gameservergroup-gameservergroupname): String
  [GameServerProtectionPolicy](#cfn-gamelift-gameservergroup-gameserverprotectionpolicy): String
  [InstanceDefinitions](#cfn-gamelift-gameservergroup-instancedefinitions): 
    InstanceDefinitions
  [LaunchTemplate](#cfn-gamelift-gameservergroup-launchtemplate): 
    LaunchTemplate
  [MaxSize](#cfn-gamelift-gameservergroup-maxsize): Double
  [MinSize](#cfn-gamelift-gameservergroup-minsize): Double
  [RoleArn](#cfn-gamelift-gameservergroup-rolearn): String
  [Tags](#cfn-gamelift-gameservergroup-tags): 
    Tags
  [VpcSubnets](#cfn-gamelift-gameservergroup-vpcsubnets): 
    VpcSubnets
```

## Properties<a name="aws-resource-gamelift-gameservergroup-properties"></a>

`AutoScalingPolicy`  <a name="cfn-gamelift-gameservergroup-autoscalingpolicy"></a>
Configuration settings to define a scaling policy optimized for game hosting\. Using the metric `"PercentUtilizedGameServers"`, this scaling policy is designed to maintain a buffer of idle game servers that can accommodate spikes in player demand\. After the game server group and Auto Scaling group are created, update the scaling policy settings directly using the **Auto Scaling Groups** console or APIs\.  
*Required*: No  
*Type*: [AutoScalingPolicy](aws-properties-gamelift-gameservergroup-autoscalingpolicy.md)  
*Update requires*: Updates are not supported\.

`BalancingStrategy`  <a name="cfn-gamelift-gameservergroup-balancingstrategy"></a>
Indicates how GameLift FleetIQ balances the use of Spot Instances and On\-Demand Instances in the game server group\. Method options include the following:   
+  `SPOT_ONLY` \- Only Spot Instances are used in the game server group\. If Spot Instances are unavailable or not viable for game hosting, the game server group provides no hosting capacity until Spot Instances can again be used\. Until then, no new instances are started, and the existing nonviable Spot Instances are terminated \(after current gameplay ends\) and are not replaced\.
+  `SPOT_PREFERRED` \- \(default value\) Spot Instances are used whenever available in the game server group\. If Spot Instances are unavailable, the game server group continues to provide hosting capacity by falling back to On\-Demand Instances\. Existing nonviable Spot Instances are terminated \(after current gameplay ends\) and are replaced with new On\-Demand Instances\. 
+ `ON_DEMAND_ONLY` \- Only On\-Demand Instances are used in the game server group\. No Spot Instances are used, even when available, while this balancing strategy is in force\.
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND_ONLY | SPOT_ONLY | SPOT_PREFERRED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeleteOption`  <a name="cfn-gamelift-gameservergroup-deleteoption"></a>
The type of stack delete to perform\. If you want to delete a stack with a non\-default delete type, first update the stack with the preferred delete type, and then delete the stack\. Delete options include:  
+  `SAFE_DELETE` – \(default\) Terminates the game server group and EC2 Auto Scaling group only when it has no game servers that are in `UTILIZED` status\.
+  `FORCE_DELETE` – Terminates the game server group, including all active game servers regardless of their utilization status, and the EC2 Auto Scaling group\. 
+  `RETAIN` – Does a safe delete of the game server group but retains the EC2 Auto Scaling group as is\.
*Required*: No  
*Type*: String  
*Allowed values*: `FORCE_DELETE | RETAIN | SAFE_DELETE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GameServerGroupName`  <a name="cfn-gamelift-gameservergroup-gameservergroupname"></a>
A developer\-defined identifier for the game server group\. The name is unique for each Region in each AWS account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-\.]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GameServerProtectionPolicy`  <a name="cfn-gamelift-gameservergroup-gameserverprotectionpolicy"></a>
A flag that indicates whether instances in the game server group are protected from early termination\. Unprotected instances that have active game servers running might be terminated during a scale\-down event, causing players to be dropped from the game\. Protected instances cannot be terminated while there are active game servers running except in the event of a forced game server group deletion\. An exception to this is Spot Instances, which can be terminated by AWS regardless of protection status\.  
*Required*: No  
*Type*: String  
*Allowed values*: `FULL_PROTECTION | NO_PROTECTION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceDefinitions`  <a name="cfn-gamelift-gameservergroup-instancedefinitions"></a>
The set of EC2 instance types that GameLift FleetIQ can use when rebalancing and automatically scaling instances in the group\. A game server group must specify at least two instance types\.  
*Required*: Yes  
*Type*: [InstanceDefinitions](aws-properties-gamelift-gameservergroup-instancedefinitions.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-gamelift-gameservergroup-launchtemplate"></a>
The EC2 launch template that contains configuration settings and game server code to be deployed to all instances in the game server group\. You can specify the template using either the template name or ID\. For help with creating a launch template, see [Creating a Launch Template for an Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon EC2 Auto Scaling User Guide*\. After the game server and Auto Scaling groups are created, update this property directly using the **Auto Scaling Groups** console or APIs\.  
*Required*: Yes  
*Type*: [LaunchTemplate](aws-properties-gamelift-gameservergroup-launchtemplate.md)  
*Update requires*: Updates are not supported\.

`MaxSize`  <a name="cfn-gamelift-gameservergroup-maxsize"></a>
The maximum number of instances allowed in the EC2 Auto Scaling group\. During automatic scaling events, GameLift FleetIQ and EC2 do not scale up the group above this maximum\. After the game server and Auto Scaling groups are created, update this property directly using the **Auto Scaling Groups** console or APIs\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: Updates are not supported\.

`MinSize`  <a name="cfn-gamelift-gameservergroup-minsize"></a>
The minimum number of instances allowed in the EC2 Auto Scaling group\. During automatic scaling events, GameLift FleetIQ and EC2 do not scale down the group below this minimum\. In production, this value should be set to at least 1\. After the game server and Auto Scaling groups are created, update this property directly using the **Auto Scaling Groups** console or APIs\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Update requires*: Updates are not supported\.

`RoleArn`  <a name="cfn-gamelift-gameservergroup-rolearn"></a>
The Amazon Resource Name \([ARN](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-arn-format.html)\) for an IAM role that allows Amazon GameLift to access your EC2 Auto Scaling groups\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:.*:role\/[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-gamelift-gameservergroup-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [Tags](aws-properties-gamelift-gameservergroup-tags.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSubnets`  <a name="cfn-gamelift-gameservergroup-vpcsubnets"></a>
A list of virtual private cloud \(VPC\) subnets to use with instances in the game server group\. By default, all GameLift FleetIQ\-supported Availability Zones are used\. You can use this parameter to specify VPCs that you've set up\. This property cannot be updated after the game server group is created, and the corresponding Auto Scaling group will always use the property value that is set with this request, even if the Auto Scaling group is updated directly\.  
*Required*: No  
*Type*: [VpcSubnets](aws-properties-gamelift-gameservergroup-vpcsubnets.md)  
*Maximum*: `20`  
*Update requires*: Updates are not supported\.

## Return values<a name="aws-resource-gamelift-gameservergroup-return-values"></a>

### Ref<a name="aws-resource-gamelift-gameservergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns unique Amazon Resource Name \(ARN\) assigned to the game server group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-gameservergroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-gameservergroup-return-values-fn--getatt-fn--getatt"></a>

`AutoScalingGroupArn`  <a name="AutoScalingGroupArn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`GameServerGroupArn`  <a name="GameServerGroupArn-fn::getatt"></a>
The unique Amazon Resource Name \(ARN\) assigned to the game server group\.

## Examples<a name="aws-resource-gamelift-gameservergroup--examples"></a>

### Create a FleetIQ game server group<a name="aws-resource-gamelift-gameservergroup--examples--Create_a_FleetIQ_game_server_group"></a>

The following example creates a game server group and and Auto Scaling group that deploys your game server software to Spot instances using two different instance types\. The game server group is set up to use Spot Instances only, so if no Spot Instances of these types are available, the game server group will effectively not start new game servers until Spot resources are available again\. The example request also triggers creation of a target\-tracking Auto Scaling policy\. With this policy, the Auto Scaling group maintains approximately 75% game server utilization\. The 25% of idle capacity enables the game server group to immediately accommodate sudden increases in player demand\. 

#### JSON<a name="aws-resource-gamelift-gameservergroup--examples--Create_a_FleetIQ_game_server_group--json"></a>

```
{
    "Resources": {
        "GameServerGroupResource": {
            "Type": "AWS::GameLift::GameServerGroup",
            "Properties": {
                "GameServerGroupName": "MegaFrogServers_NA",
                "RoleArn": "arn:aws:iam:123456789012::role/GameLiftGsgRole",
                "MinSize": 1,
                "MaxSize": 1000,
                "GameServerProtectionPolicy": "NO_PROTECTION",
                "BalancingStrategy": "SPOT_ONLY",
                "LaunchTemplate": { 
                "LaunchTemplateId": "lt-1234567890abcdef",
                },
                "InstanceDefinitions": [ 
                    {"InstanceType": "c5.xlarge"},
                    {"InstanceType": "m5.xlarge"}
                ],
                "AutoScalingPolicy": { 
                    "TargetTrackingConfiguration": { 
                        "TargetValue": 75
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-gameservergroup--examples--Create_a_FleetIQ_game_server_group--yaml"></a>

```
Resources:
    GameServerGroupResource:
        Type: AWS::GameLift::GameServerGroup
        Properties:
            GameServerGroupName: "MegaFrogServers_NA"
            RoleArn: !GetAtt IAMRole.Arn
            MinSize: 1
            MaxSize: 1000
            GameServerProtectionPolicy: "NO_PROTECTION"
            BalancingStrategy: "SPOT_ONLY"
            LaunchTemplate: 
                LaunchTemplateId: "lt-1234567890abcdef"
            InstanceDefinitions:  
                - InstanceType: "c5.xlarge"
                - InstanceType: "m5.xlarge"
            AutoScalingPolicy: 
                TargetTrackingConfiguration:
                    TargetValue: 75
```

## See also<a name="aws-resource-gamelift-gameservergroup--seealso"></a>
+  [GameLift FleetIQ Guide](https://docs.aws.amazon.com/gamelift/latest/developerguide/gsg-intro.html) 
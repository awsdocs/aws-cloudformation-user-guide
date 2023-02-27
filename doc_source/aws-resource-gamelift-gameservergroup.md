# AWS::GameLift::GameServerGroup<a name="aws-resource-gamelift-gameservergroup"></a>

 **This operation is used with the Amazon GameLift FleetIQ solution and game server groups\.** 

Creates a GameLift FleetIQ game server group for managing game hosting on a collection of Amazon EC2 instances for game hosting\. This operation creates the game server group, creates an Auto Scaling group in your AWS account, and establishes a link between the two groups\. You can view the status of your game server groups in the GameLift console\. Game server group metrics and events are emitted to Amazon CloudWatch\.

Before creating a new game server group, you must have the following: 
+ An Amazon EC2 launch template that specifies how to launch Amazon EC2 instances with your game server build\. For more information, see [ Launching an Instance from a Launch Template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html) in the *Amazon EC2 User Guide*\. 
+ An IAM role that extends limited access to your AWS account to allow GameLift FleetIQ to create and interact with the Auto Scaling group\. For more information, see [Create IAM roles for cross\-service interaction](https://docs.aws.amazon.com/gamelift/latest/fleetiqguide/gsg-iam-permissions-roles.html) in the *GameLift FleetIQ Developer Guide*\.

To create a new game server group, specify a unique group name, IAM role and Amazon EC2 launch template, and provide a list of instance types that can be used in the group\. You must also set initial maximum and minimum limits on the group's instance count\. You can optionally set an Auto Scaling policy with target tracking based on a GameLift FleetIQ metric\.

Once the game server group and corresponding Auto Scaling group are created, you have full access to change the Auto Scaling group's configuration as needed\. Several properties that are set when creating a game server group, including maximum/minimum size and auto\-scaling policy settings, must be updated directly in the Auto Scaling group\. Keep in mind that some Auto Scaling group properties are periodically updated by GameLift FleetIQ as part of its balancing activities to optimize for availability and cost\.

 **Learn more** 

 [GameLift FleetIQ Guide](https://docs.aws.amazon.com/gamelift/latest/fleetiqguide/gsg-intro.html) 

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
      "[InstanceDefinitions](#cfn-gamelift-gameservergroup-instancedefinitions)" : [ InstanceDefinition, ... ],
      "[LaunchTemplate](#cfn-gamelift-gameservergroup-launchtemplate)" : LaunchTemplate,
      "[MaxSize](#cfn-gamelift-gameservergroup-maxsize)" : Double,
      "[MinSize](#cfn-gamelift-gameservergroup-minsize)" : Double,
      "[RoleArn](#cfn-gamelift-gameservergroup-rolearn)" : String,
      "[Tags](#cfn-gamelift-gameservergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcSubnets](#cfn-gamelift-gameservergroup-vpcsubnets)" : [ String, ... ]
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
    - InstanceDefinition
  [LaunchTemplate](#cfn-gamelift-gameservergroup-launchtemplate): 
    LaunchTemplate
  [MaxSize](#cfn-gamelift-gameservergroup-maxsize): Double
  [MinSize](#cfn-gamelift-gameservergroup-minsize): Double
  [RoleArn](#cfn-gamelift-gameservergroup-rolearn): String
  [Tags](#cfn-gamelift-gameservergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcSubnets](#cfn-gamelift-gameservergroup-vpcsubnets): 
    - String
```

## Properties<a name="aws-resource-gamelift-gameservergroup-properties"></a>

`AutoScalingPolicy`  <a name="cfn-gamelift-gameservergroup-autoscalingpolicy"></a>
Configuration settings to define a scaling policy for the Auto Scaling group that is optimized for game hosting\. The scaling policy uses the metric `"PercentUtilizedGameServers"` to maintain a buffer of idle game servers that can immediately accommodate new games and players\. After the Auto Scaling group is created, update this value directly in the Auto Scaling group using the AWS console or APIs\.  
*Required*: No  
*Type*: [AutoScalingPolicy](aws-properties-gamelift-gameservergroup-autoscalingpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BalancingStrategy`  <a name="cfn-gamelift-gameservergroup-balancingstrategy"></a>
Indicates how GameLift FleetIQ balances the use of Spot Instances and On\-Demand Instances in the game server group\. Method options include the following:  
+  `SPOT_ONLY` \- Only Spot Instances are used in the game server group\. If Spot Instances are unavailable or not viable for game hosting, the game server group provides no hosting capacity until Spot Instances can again be used\. Until then, no new instances are started, and the existing nonviable Spot Instances are terminated \(after current gameplay ends\) and are not replaced\.
+  `SPOT_PREFERRED` \- \(default value\) Spot Instances are used whenever available in the game server group\. If Spot Instances are unavailable, the game server group continues to provide hosting capacity by falling back to On\-Demand Instances\. Existing nonviable Spot Instances are terminated \(after current gameplay ends\) and are replaced with new On\-Demand Instances\.
+  `ON_DEMAND_ONLY` \- Only On\-Demand Instances are used in the game server group\. No Spot Instances are used, even when available, while this balancing strategy is in force\.
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND_ONLY | SPOT_ONLY | SPOT_PREFERRED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeleteOption`  <a name="cfn-gamelift-gameservergroup-deleteoption"></a>
The type of delete to perform\. To delete a game server group, specify the `DeleteOption`\. Options include the following:  
+  `SAFE_DELETE` – \(default\) Terminates the game server group and Amazon EC2 Auto Scaling group only when it has no game servers that are in `UTILIZED` status\.
+  `FORCE_DELETE` – Terminates the game server group, including all active game servers regardless of their utilization status, and the Amazon EC2 Auto Scaling group\. 
+  `RETAIN` – Does a safe delete of the game server group but retains the Amazon EC2 Auto Scaling group as is\.
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
A flag that indicates whether instances in the game server group are protected from early termination\. Unprotected instances that have active game servers running might be terminated during a scale\-down event, causing players to be dropped from the game\. Protected instances cannot be terminated while there are active game servers running except in the event of a forced game server group deletion \(see \)\. An exception to this is with Spot Instances, which can be terminated by AWS regardless of protection status\.   
*Required*: No  
*Type*: String  
*Allowed values*: `FULL_PROTECTION | NO_PROTECTION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceDefinitions`  <a name="cfn-gamelift-gameservergroup-instancedefinitions"></a>
The set of Amazon EC2 instance types that GameLift FleetIQ can use when balancing and automatically scaling instances in the corresponding Auto Scaling group\.   
*Required*: Yes  
*Type*: List of [InstanceDefinition](aws-properties-gamelift-gameservergroup-instancedefinition.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-gamelift-gameservergroup-launchtemplate"></a>
The Amazon EC2 launch template that contains configuration settings and game server code to be deployed to all instances in the game server group\. You can specify the template using either the template name or ID\. For help with creating a launch template, see [Creating a Launch Template for an Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon Elastic Compute Cloud Auto Scaling User Guide*\. After the Auto Scaling group is created, update this value directly in the Auto Scaling group using the AWS console or APIs\.  
If you specify network interfaces in your launch template, you must explicitly set the property `AssociatePublicIpAddress` to "true"\. If no network interface is specified in the launch template, GameLift FleetIQ uses your account's default VPC\.
*Required*: Yes  
*Type*: [LaunchTemplate](aws-properties-gamelift-gameservergroup-launchtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-gamelift-gameservergroup-maxsize"></a>
The maximum number of instances allowed in the Amazon EC2 Auto Scaling group\. During automatic scaling events, GameLift FleetIQ and EC2 do not scale up the group above this maximum\. After the Auto Scaling group is created, update this value directly in the Auto Scaling group using the AWS console or APIs\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-gamelift-gameservergroup-minsize"></a>
The minimum number of instances allowed in the Amazon EC2 Auto Scaling group\. During automatic scaling events, GameLift FleetIQ and Amazon EC2 do not scale down the group below this minimum\. In production, this value should be set to at least 1\. After the Auto Scaling group is created, update this value directly in the Auto Scaling group using the AWS console or APIs\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-gamelift-gameservergroup-rolearn"></a>
The Amazon Resource Name \([ARN](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-arn-format.html)\) for an IAM role that allows Amazon GameLift to access your Amazon EC2 Auto Scaling groups\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:.*:role\/[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-gamelift-gameservergroup-tags"></a>
A list of labels to assign to the new game server group resource\. Tags are developer\-defined key\-value pairs\. Tagging AWS resources is useful for resource management, access management, and cost allocation\. For more information, see [ Tagging AWS Resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in the * AWS General Reference*\. Once the resource is created, you can use TagResource, UntagResource, and ListTagsForResource to add, remove, and view tags, respectively\. The maximum tag limit may be lower than stated\. See the AWS General Reference for actual tagging limits\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSubnets`  <a name="cfn-gamelift-gameservergroup-vpcsubnets"></a>
A list of virtual private cloud \(VPC\) subnets to use with instances in the game server group\. By default, all GameLift FleetIQ\-supported Availability Zones are used\. You can use this parameter to specify VPCs that you've set up\. This property cannot be updated after the game server group is created, and the corresponding Auto Scaling group will always use the property value that is set with this request, even if the Auto Scaling group is updated directly\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-gamelift-gameservergroup-return-values"></a>

### Ref<a name="aws-resource-gamelift-gameservergroup-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-gamelift-gameservergroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-gameservergroup-return-values-fn--getatt-fn--getatt"></a>

`AutoScalingGroupArn`  <a name="AutoScalingGroupArn-fn::getatt"></a>
A unique identifier for the auto scaling group\.

`GameServerGroupArn`  <a name="GameServerGroupArn-fn::getatt"></a>
A unique identifier for the game server group\.
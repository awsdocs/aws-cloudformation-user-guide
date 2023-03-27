# AWS::AutoScaling::WarmPool<a name="aws-resource-autoscaling-warmpool"></a>

The `AWS::AutoScaling::WarmPool` resource creates a pool of pre\-initialized EC2 instances that sits alongside the Auto Scaling group\. Whenever your application needs to scale out, the Auto Scaling group can draw on the warm pool to meet its new desired capacity\. 

When you create a warm pool, you can define a minimum size\. When your Auto Scaling group scales out and the size of the warm pool shrinks, Amazon EC2 Auto Scaling launches new instances into the warm pool to maintain its minimum size\. 

For more information, see [Warm pools for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-warm-pools.html) in the *Amazon EC2 Auto Scaling User Guide*\.

**Note**  
CloudFormation supports the `UpdatePolicy` attribute for Auto Scaling groups\. During an update, if `UpdatePolicy` is set to `AutoScalingRollingUpdate`, CloudFormation replaces `InService` instances only\. Instances in the warm pool are not replaced\. The difference in which instances are replaced can potentially result in different instance configurations after the stack update completes\. If `UpdatePolicy` is set to `AutoScalingReplacingUpdate`, you do not encounter this issue because CloudFormation replaces both the Auto Scaling group and the warm pool\.

## Syntax<a name="aws-resource-autoscaling-warmpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-warmpool-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::WarmPool",
  "Properties" : {
      "[AutoScalingGroupName](#cfn-autoscaling-warmpool-autoscalinggroupname)" : String,
      "[InstanceReusePolicy](#cfn-autoscaling-warmpool-instancereusepolicy)" : InstanceReusePolicy,
      "[MaxGroupPreparedCapacity](#cfn-autoscaling-warmpool-maxgrouppreparedcapacity)" : Integer,
      "[MinSize](#cfn-autoscaling-warmpool-minsize)" : Integer,
      "[PoolState](#cfn-autoscaling-warmpool-poolstate)" : String
    }
}
```

### YAML<a name="aws-resource-autoscaling-warmpool-syntax.yaml"></a>

```
Type: AWS::AutoScaling::WarmPool
Properties: 
  [AutoScalingGroupName](#cfn-autoscaling-warmpool-autoscalinggroupname): String
  [InstanceReusePolicy](#cfn-autoscaling-warmpool-instancereusepolicy): 
    InstanceReusePolicy
  [MaxGroupPreparedCapacity](#cfn-autoscaling-warmpool-maxgrouppreparedcapacity): Integer
  [MinSize](#cfn-autoscaling-warmpool-minsize): Integer
  [PoolState](#cfn-autoscaling-warmpool-poolstate): String
```

## Properties<a name="aws-resource-autoscaling-warmpool-properties"></a>

`AutoScalingGroupName`  <a name="cfn-autoscaling-warmpool-autoscalinggroupname"></a>
The name of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceReusePolicy`  <a name="cfn-autoscaling-warmpool-instancereusepolicy"></a>
Indicates whether instances in the Auto Scaling group can be returned to the warm pool on scale in\. The default is to terminate instances in the Auto Scaling group when the group scales in\.  
*Required*: No  
*Type*: [InstanceReusePolicy](aws-properties-autoscaling-warmpool-instancereusepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxGroupPreparedCapacity`  <a name="cfn-autoscaling-warmpool-maxgrouppreparedcapacity"></a>
Specifies the maximum number of instances that are allowed to be in the warm pool or in any state except `Terminated` for the Auto Scaling group\. This is an optional property\. Specify it only if you do not want the warm pool size to be determined by the difference between the group's maximum capacity and its desired capacity\.   
If a value for `MaxGroupPreparedCapacity` is not specified, Amazon EC2 Auto Scaling launches and maintains the difference between the group's maximum capacity and its desired capacity\. If you specify a value for `MaxGroupPreparedCapacity`, Amazon EC2 Auto Scaling uses the difference between the `MaxGroupPreparedCapacity` and the desired capacity instead\.   
The size of the warm pool is dynamic\. Only when `MaxGroupPreparedCapacity` and `MinSize` are set to the same value does the warm pool have an absolute size\.
If the desired capacity of the Auto Scaling group is higher than the `MaxGroupPreparedCapacity`, the capacity of the warm pool is 0, unless you specify a value for `MinSize`\. To remove a value that you previously set, include the property but specify \-1 for the value\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `-1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-autoscaling-warmpool-minsize"></a>
Specifies the minimum number of instances to maintain in the warm pool\. This helps you to ensure that there is always a certain number of warmed instances available to handle traffic spikes\. Defaults to 0 if not specified\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PoolState`  <a name="cfn-autoscaling-warmpool-poolstate"></a>
Sets the instance state to transition to after the lifecycle actions are complete\. Default is `Stopped`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Hibernated | Running | Stopped`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Remarks<a name="aws-resource-autoscaling-warmpool--remarks"></a>

CloudFormation won't mark the warm pool as successful \(by setting its status to CREATE\_COMPLETE\) if there are lifecycle hooks that haven't been completed\. If the state of an instance is `Warmed:Pending:Wait`, the lifeycle hook is not considered complete\. For more information, see [Use lifecycle hooks with a warm pool](https://docs.aws.amazon.com/autoscaling/ec2/userguide/warm-pool-instance-lifecycle.html) in the *Amazon EC2 Auto Scaling User Guide*\.

If you want to hibernate instances on scale in and there are existing instances in the Auto Scaling group, they must meet the requirements for instance hibernation\. If they don't, when instances return to the warm pool, they will fallback to being stopped instead of being hibernated\.

## Examples<a name="aws-resource-autoscaling-warmpool--examples"></a>

The following example defines a warm pool for an Auto Scaling group\.

For more template snippets, see our [GitHub repository](https://github.com/aws-samples/amazon-ec2-auto-scaling-group-examples)\. Included are examples of lifecycle hooks that work with warm pools\. 

### Auto Scaling group with warm pool<a name="aws-resource-autoscaling-warmpool--examples--Auto_Scaling_group_with_warm_pool"></a>

The following template snippet shows an `AWS::AutoScaling::WarmPool` resource for an Auto Scaling group where you specify values for the `MinSize` and `PoolState` properties\. 

#### JSON<a name="aws-resource-autoscaling-warmpool--examples--Auto_Scaling_group_with_warm_pool--json"></a>

```
{
  "Resources":{
    "myWarmPool":{
      "Type":"AWS::AutoScaling::WarmPool",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "MinSize":30,
        "PoolState":"Stopped"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-warmpool--examples--Auto_Scaling_group_with_warm_pool--yaml"></a>

```
---
Resources:
  myWarmPool: 
    Type: AWS::AutoScaling::WarmPool
    Properties:
      AutoScalingGroupName: !Ref myASG
      MinSize: '30'
      PoolState: Stopped
```

## See also<a name="aws-resource-autoscaling-warmpool--seealso"></a>
+ [PutWarmPool](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutWarmPool.html) in the *Amazon EC2 Auto Scaling API Reference*
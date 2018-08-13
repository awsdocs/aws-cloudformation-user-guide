# AWS::AutoScaling::ScheduledAction<a name="aws-resource-as-scheduledaction"></a>

Creates a scheduled scaling action for an Auto Scaling group, changing the number of servers available for your application in response to predictable load changes\.

**Important**  
If you have rolling updates enabled, you must suspend scheduled actions before you can update the Auto Scaling group\. You can suspend processes by using the [UpdatePolicy attribute](aws-attribute-updatepolicy.md) for the `AWS::AutoScaling::AutoScalingGroup` resource \(recommended\), the AWS CLI, or the Amazon EC2 Auto Scaling API\. For more information about suspending scheduled actions, see [Suspending and Resuming Scaling Processes](http://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html) in the *Amazon EC2 Auto Scaling User Guide*\.
When you update a stack with an Auto Scaling group and scheduled action, AWS CloudFormation always sets the min size, max size, and desired capacity properties of your Auto Scaling group to the values that are defined in the `AWS::AutoScaling::AutoScalingGroup` resource of your template, even if a scheduled action is in effect\. However, you might not want AWS CloudFormation to change any of the group size property values, such as when you have a scheduled action in effect\. You can use an [UpdatePolicy attribute](aws-attribute-updatepolicy.md) to prevent AWS CloudFormation from changing the min size, max size, or desired capacity property values during a stack update unless you modified the individual values in your template\.

**Topics**
+ [Syntax](#aws-resource-autoscaling-scheduledaction-syntax)
+ [Properties](#w3ab2c21c10d148c11)
+ [Return Value](#w3ab2c21c10d148c13)
+ [Auto Scaling Scheduled Action Snippet](#w3ab2c21c10d148c15)

## Syntax<a name="aws-resource-autoscaling-scheduledaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-scheduledaction-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::ScheduledAction",
  "Properties" : {
    "[AutoScalingGroupName](#cfn-as-scheduledaction-asgname)" : String,
    "[DesiredCapacity](#cfn-as-scheduledaction-desiredcapacity)" : Integer,
    "[EndTime](#cfn-as-scheduledaction-endtime)" : Time stamp,
    "[MaxSize](#cfn-as-scheduledaction-maxsize)" : Integer,
    "[MinSize](#cfn-as-scheduledaction-minsize)" : Integer,
    "[Recurrence](#cfn-as-scheduledaction-recurrence)" : String,
    "[StartTime](#cfn-as-scheduledaction-starttime)" : Time stamp
  }
}
```

### YAML<a name="aws-resource-autoscaling-scheduledaction-syntax.yaml"></a>

```
Type: AWS::AutoScaling::ScheduledAction
Properties:
  [AutoScalingGroupName](#cfn-as-scheduledaction-asgname): String
  [DesiredCapacity](#cfn-as-scheduledaction-desiredcapacity): Integer
  [EndTime](#cfn-as-scheduledaction-endtime): Time stamp
  [MaxSize](#cfn-as-scheduledaction-maxsize): Integer
  [MinSize](#cfn-as-scheduledaction-minsize): Integer
  [Recurrence](#cfn-as-scheduledaction-recurrence): String
  [StartTime](#cfn-as-scheduledaction-starttime): Time stamp
```

## Properties<a name="w3ab2c21c10d148c11"></a>

`AutoScalingGroupName`  <a name="cfn-as-scheduledaction-asgname"></a>
The name or ARN of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DesiredCapacity`  <a name="cfn-as-scheduledaction-desiredcapacity"></a>
The number of Amazon EC2 instances that should be running in the Auto Scaling group\. At least one of `MaxSize`, `MinSize`, or `DesiredCapacity` must be specified\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EndTime`  <a name="cfn-as-scheduledaction-endtime"></a>
The time in UTC for this schedule to end\. For example, `2010-06-01T00:00:00Z`\.  
*Required*: No  
*Type*: Time stamp  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MaxSize`  <a name="cfn-as-scheduledaction-maxsize"></a>
The maximum number of Amazon EC2 instances in the Auto Scaling group\. At least one of `MaxSize`, `MinSize`, or `DesiredCapacity` must be specified\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MinSize`  <a name="cfn-as-scheduledaction-minsize"></a>
The minimum number of Amazon EC2 instances in the Auto Scaling group\. At least one of `MaxSize`, `MinSize`, or `DesiredCapacity` must be specified\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Recurrence`  <a name="cfn-as-scheduledaction-recurrence"></a>
The time in UTC when recurring future actions will start\. You specify the start time by following the Unix cron syntax format\. For more information about cron syntax, go to [http://en\.wikipedia\.org/wiki/Cron](http://en.wikipedia.org/wiki/Cron)\.  
Specifying the `StartTime` and `EndTime` properties with `Recurrence` property forms the start and stop boundaries of the recurring action\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StartTime`  <a name="cfn-as-scheduledaction-starttime"></a>
The time in UTC for this schedule to start\. For example, `2010-06-01T00:00:00Z`\.  
*Required*: No  
*Type*: Time stamp  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d148c13"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyScheduledAction" }
```

For a scheduled Auto Scaling action with the logical ID `MyScheduledAction`, `Ref` returns the scheduled action name\. For example:

`mystack-myscheduledaction-NT5EUXTNTXXD`

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Auto Scaling Scheduled Action Snippet<a name="w3ab2c21c10d148c15"></a>

The following template snippet includes two scheduled actions that scale the number of instances in an Auto Scaling group\. The `ScheduledActionUp` action starts at 7 AM every day and sets the Auto Scaling group to a minimum of five Amazon EC2 instances with a maximum of 10\. The `ScheduledActionDown` action starts at 7 PM every day and sets the Auto Scaling group to a minimum and maximum of one Amazon EC2 instance\.

### JSON<a name="aws-resource-autoscaling-scheduledaction-example.json"></a>

```
"ScheduledActionUp": {
  "Type": "AWS::AutoScaling::ScheduledAction",
  "Properties": {
    "AutoScalingGroupName": {
      "Ref": "WebServerGroup"
    },
    "MaxSize": "10",
    "MinSize": "5",
    "Recurrence": "0 7 * * *"
  }
},
"ScheduledActionDown": {
  "Type": "AWS::AutoScaling::ScheduledAction",
  "Properties": {
    "AutoScalingGroupName": {
      "Ref": "WebServerGroup"
    },
    "MaxSize": "1",
    "MinSize": "1",
    "Recurrence": "0 19 * * *"
  }
}
```

### YAML<a name="aws-resource-autoscaling-scheduledaction-example.yaml"></a>

```
ScheduledActionUp: 
  Type: "AWS::AutoScaling::ScheduledAction"
  Properties:
    AutoScalingGroupName: 
      Ref: "WebServerGroup"
    MaxSize: 10
    MinSize: 5
    Recurrence: "0 7 * * *"
ScheduledActionDown: 
  Type: "AWS::AutoScaling::ScheduledAction"
  Properties:
    AutoScalingGroupName: 
      Ref: "WebServerGroup"
    MaxSize: 1
    MinSize: 1
    Recurrence: "0 19 * * *"
```
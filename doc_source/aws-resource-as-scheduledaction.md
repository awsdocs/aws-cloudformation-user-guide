# AWS::AutoScaling::ScheduledAction<a name="aws-resource-as-scheduledaction"></a>

The AWS::AutoScaling::ScheduledAction resource specifies an Amazon EC2 Auto Scaling scheduled action so that the Auto Scaling group can change the number of instances available for your application in response to predictable load changes\. 

When you update a stack with an Auto Scaling group and scheduled action, AWS CloudFormation always sets the min size, max size, and desired capacity properties of your group to the values that are defined in the `AWS::AutoScaling::AutoScalingGroup` section of your template\. However, you might not want CloudFormation to do that when you have a scheduled action in effect\. You can use an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) to prevent CloudFormation from changing the min size, max size, or desired capacity property values during a stack update unless you modified the individual values in your template\. If you have rolling updates enabled, before you can update the Auto Scaling group, you must suspend scheduled actions by specifying an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the Auto Scaling group\. You can find sample update policies for rolling updates in [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

For more information, see [Scheduled scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html) and [Suspending and resuming scaling processes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-resource-as-scheduledaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-as-scheduledaction-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::ScheduledAction",
  "Properties" : {
      "[AutoScalingGroupName](#cfn-as-scheduledaction-asgname)" : String,
      "[DesiredCapacity](#cfn-as-scheduledaction-desiredcapacity)" : Integer,
      "[EndTime](#cfn-as-scheduledaction-endtime)" : String,
      "[MaxSize](#cfn-as-scheduledaction-maxsize)" : Integer,
      "[MinSize](#cfn-as-scheduledaction-minsize)" : Integer,
      "[Recurrence](#cfn-as-scheduledaction-recurrence)" : String,
      "[StartTime](#cfn-as-scheduledaction-starttime)" : String
    }
}
```

### YAML<a name="aws-resource-as-scheduledaction-syntax.yaml"></a>

```
Type: AWS::AutoScaling::ScheduledAction
Properties: 
  [AutoScalingGroupName](#cfn-as-scheduledaction-asgname): String
  [DesiredCapacity](#cfn-as-scheduledaction-desiredcapacity): Integer
  [EndTime](#cfn-as-scheduledaction-endtime): String
  [MaxSize](#cfn-as-scheduledaction-maxsize): Integer
  [MinSize](#cfn-as-scheduledaction-minsize): Integer
  [Recurrence](#cfn-as-scheduledaction-recurrence): String
  [StartTime](#cfn-as-scheduledaction-starttime): String
```

## Properties<a name="aws-resource-as-scheduledaction-properties"></a>

`AutoScalingGroupName`  <a name="cfn-as-scheduledaction-asgname"></a>
The name or Amazon Resource Name \(ARN\) of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DesiredCapacity`  <a name="cfn-as-scheduledaction-desiredcapacity"></a>
The desired capacity is the initial capacity of the Auto Scaling group after the scheduled action runs and the capacity it attempts to maintain\. It can scale beyond this capacity if you add more scaling conditions\.  
You must specify at least one of the following properties: `MaxSize`, `MinSize`, or `DesiredCapacity`\.   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndTime`  <a name="cfn-as-scheduledaction-endtime"></a>
The date and time in UTC for the recurring schedule to end\. For example, `"2019-06-01T00:00:00Z"`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-as-scheduledaction-maxsize"></a>
The maximum size of the Auto Scaling group\.  
You must specify at least one of the following properties: `MaxSize`, `MinSize`, or `DesiredCapacity`\.   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-as-scheduledaction-minsize"></a>
The minimum size of the Auto Scaling group\.  
You must specify at least one of the following properties: `MaxSize`, `MinSize`, or `DesiredCapacity`\.   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Recurrence`  <a name="cfn-as-scheduledaction-recurrence"></a>
The recurring schedule for this action, in Unix cron syntax format\. For more information about cron syntax, see [Crontab](http://crontab.org/)\.   
Specifying the `StartTime` and `EndTime` properties with `Recurrence` property forms the start and stop boundaries of the recurring action\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-as-scheduledaction-starttime"></a>
The date and time in UTC for this action to start\. For example, `"2019-06-01T00:00:00Z"`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-as-scheduledaction-return-values"></a>

### Ref<a name="aws-resource-as-scheduledaction-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-myscheduledaction-NT5EUXTNTXXD`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-as-scheduledaction--examples"></a>

The following example schedule scaling actions for an Auto Scaling group\.

### Scheduled scaling action<a name="aws-resource-as-scheduledaction--examples--Scheduled_scaling_action"></a>

The following template snippet includes two scheduled actions that scale the number of instances in an Auto Scaling group\. The `ScheduledActionOut` action starts at 7 AM every day and sets the Auto Scaling group to a minimum of five Amazon EC2 instances with a maximum of 10\. The `ScheduledActionIn` action starts at 7 PM every day and sets the Auto Scaling group to a minimum and maximum of one Amazon EC2 instance\. 

#### JSON<a name="aws-resource-as-scheduledaction--examples--Scheduled_scaling_action--json"></a>

```
{
  "Resources":{
    "ScheduledActionOut":{
      "Type":"AWS::AutoScaling::ScheduledAction",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "MaxSize":"10",
        "MinSize":"5",
        "Recurrence":"0 7 * * *"
      }
    },
    "ScheduledActionIn":{
      "Type":"AWS::AutoScaling::ScheduledAction",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "MaxSize":"1",
        "MinSize":"1",
        "Recurrence":"0 19 * * *"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-as-scheduledaction--examples--Scheduled_scaling_action--yaml"></a>

```
---
Resources:
  ScheduledActionOut: 
    Type: AWS::AutoScaling::ScheduledAction
    Properties:
      AutoScalingGroupName: 
        Ref: "myASG"
      MaxSize: 10
      MinSize: 5
      Recurrence: "0 7 * * *"
  ScheduledActionIn: 
    Type: AWS::AutoScaling::ScheduledAction
    Properties:
      AutoScalingGroupName: 
        Ref: "myASG"
      MaxSize: 1
      MinSize: 1
      Recurrence: "0 19 * * *"
```
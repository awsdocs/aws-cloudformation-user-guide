# AWS::AutoScaling::ScheduledAction<a name="aws-resource-autoscaling-scheduledaction"></a>

The `AWS::AutoScaling::ScheduledAction` resource specifies an Amazon EC2 Auto Scaling scheduled action so that the Auto Scaling group can change the number of instances available for your application in response to predictable load changes\. 

When you update a stack with an Auto Scaling group and scheduled action, CloudFormation always sets the min size, max size, and desired capacity properties of your group to the values that are defined in the `AWS::AutoScaling::AutoScalingGroup` section of your template\. However, you might not want CloudFormation to do that when you have a scheduled action in effect\. You can use an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) to prevent CloudFormation from changing the min size, max size, or desired capacity property values during a stack update unless you modified the individual values in your template\. If you have rolling updates enabled, before you can update the Auto Scaling group, you must suspend scheduled actions by specifying an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the Auto Scaling group\. You can find a sample update policy for rolling updates in [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

For more information, see [Scheduled scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html) and [Suspending and resuming scaling processes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-resource-autoscaling-scheduledaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-scheduledaction-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::ScheduledAction",
  "Properties" : {
      "[AutoScalingGroupName](#cfn-autoscaling-scheduledaction-autoscalinggroupname)" : String,
      "[DesiredCapacity](#cfn-autoscaling-scheduledaction-desiredcapacity)" : Integer,
      "[EndTime](#cfn-autoscaling-scheduledaction-endtime)" : String,
      "[MaxSize](#cfn-autoscaling-scheduledaction-maxsize)" : Integer,
      "[MinSize](#cfn-autoscaling-scheduledaction-minsize)" : Integer,
      "[Recurrence](#cfn-autoscaling-scheduledaction-recurrence)" : String,
      "[StartTime](#cfn-autoscaling-scheduledaction-starttime)" : String,
      "[TimeZone](#cfn-autoscaling-scheduledaction-timezone)" : String
    }
}
```

### YAML<a name="aws-resource-autoscaling-scheduledaction-syntax.yaml"></a>

```
Type: AWS::AutoScaling::ScheduledAction
Properties: 
  [AutoScalingGroupName](#cfn-autoscaling-scheduledaction-autoscalinggroupname): String
  [DesiredCapacity](#cfn-autoscaling-scheduledaction-desiredcapacity): Integer
  [EndTime](#cfn-autoscaling-scheduledaction-endtime): String
  [MaxSize](#cfn-autoscaling-scheduledaction-maxsize): Integer
  [MinSize](#cfn-autoscaling-scheduledaction-minsize): Integer
  [Recurrence](#cfn-autoscaling-scheduledaction-recurrence): String
  [StartTime](#cfn-autoscaling-scheduledaction-starttime): String
  [TimeZone](#cfn-autoscaling-scheduledaction-timezone): String
```

## Properties<a name="aws-resource-autoscaling-scheduledaction-properties"></a>

`AutoScalingGroupName`  <a name="cfn-autoscaling-scheduledaction-autoscalinggroupname"></a>
The name of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DesiredCapacity`  <a name="cfn-autoscaling-scheduledaction-desiredcapacity"></a>
The desired capacity is the initial capacity of the Auto Scaling group after the scheduled action runs and the capacity it attempts to maintain\. It can scale beyond this capacity if you add more scaling conditions\.   
You must specify at least one of the following properties: `MaxSize`, `MinSize`, or `DesiredCapacity`\. 
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndTime`  <a name="cfn-autoscaling-scheduledaction-endtime"></a>
The date and time for the recurring schedule to end, in UTC\. For example, `"2021-06-01T00:00:00Z"`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-autoscaling-scheduledaction-maxsize"></a>
The maximum size of the Auto Scaling group\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-autoscaling-scheduledaction-minsize"></a>
The minimum size of the Auto Scaling group\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Recurrence`  <a name="cfn-autoscaling-scheduledaction-recurrence"></a>
The recurring schedule for this action\. This format consists of five fields separated by white spaces: \[Minute\] \[Hour\] \[Day\_of\_Month\] \[Month\_of\_Year\] \[Day\_of\_Week\]\. The value must be in quotes \(for example, `"30 0 1 1,6,12 *"`\)\. For more information about this format, see [Crontab](http://crontab.org)\.  
When `StartTime` and `EndTime` are specified with `Recurrence`, they form the boundaries of when the recurring action starts and stops\.  
Cron expressions use Universal Coordinated Time \(UTC\) by default\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-autoscaling-scheduledaction-starttime"></a>
The date and time for this action to start, in YYYY\-MM\-DDThh:mm:ssZ format in UTC/GMT only and in quotes \(for example, `"2021-06-01T00:00:00Z"`\)\.  
If you specify `Recurrence` and `StartTime`, Amazon EC2 Auto Scaling performs the action at this time, and then performs the action based on the specified recurrence\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZone`  <a name="cfn-autoscaling-scheduledaction-timezone"></a>
Specifies the time zone for a cron expression\. If a time zone is not provided, UTC is used by default\.   
Valid values are the canonical names of the IANA time zones, derived from the IANA Time Zone Database \(such as `Etc/GMT+9` or `Pacific/Tahiti`\)\. For more information, see [https://en\.wikipedia\.org/wiki/List\_of\_tz\_database\_time\_zones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-autoscaling-scheduledaction-return-values"></a>

### Ref<a name="aws-resource-autoscaling-scheduledaction-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-myscheduledaction-NT5EUXTNTXXD`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-autoscaling-scheduledaction-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-autoscaling-scheduledaction-return-values-fn--getatt-fn--getatt"></a>

`ScheduledActionName`  <a name="ScheduledActionName-fn::getatt"></a>
Returns the name of a scheduled action\.

## Examples<a name="aws-resource-autoscaling-scheduledaction--examples"></a>

The following examples schedule scaling actions for an Auto Scaling group\.

### Scheduled actions that run on a recurring schedule<a name="aws-resource-autoscaling-scheduledaction--examples--Scheduled_actions_that_run_on_a_recurring_schedule"></a>

The following template snippet includes two scheduled actions that scale the number of instances in an Auto Scaling group\. The `ScheduledActionOut` action starts at 7 AM every day and sets the Auto Scaling group to a minimum of five Amazon EC2 instances with a maximum of 10\. The `ScheduledActionIn` action starts at 7 PM every day and sets the Auto Scaling group to a minimum and maximum of one Amazon EC2 instance\. The time zone is not provided\. As a result, these scheduled actions will recur in UTC time\. 

#### JSON<a name="aws-resource-autoscaling-scheduledaction--examples--Scheduled_actions_that_run_on_a_recurring_schedule--json"></a>

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

#### YAML<a name="aws-resource-autoscaling-scheduledaction--examples--Scheduled_actions_that_run_on_a_recurring_schedule--yaml"></a>

```
---
Resources:
  ScheduledActionOut: 
    Type: AWS::AutoScaling::ScheduledAction
    Properties:
      AutoScalingGroupName: !Ref myASG
      MaxSize: '10'
      MinSize: '5'
      Recurrence: "0 7 * * *"
  ScheduledActionIn: 
    Type: AWS::AutoScaling::ScheduledAction
    Properties:
      AutoScalingGroupName: !Ref myASG
      MaxSize: '1'
      MinSize: '1'
      Recurrence: "0 19 * * *"
```

### Scheduled scaling action that occurs only once<a name="aws-resource-autoscaling-scheduledaction--examples--Scheduled_scaling_action_that_occurs_only_once"></a>

The following template snippet includes a one\-time scheduled action\. At the date and time specified for `StartTime` \(4:00 PM UTC on March 31, 2021\), if the group currently has more than 1 instance, it scales in to 1 instance\. If the group currently has no instances, it scales out to 1 instance\. 

#### JSON<a name="aws-resource-autoscaling-scheduledaction--examples--Scheduled_scaling_action_that_occurs_only_once--json"></a>

```
{
  "Resources":{
    "OneTimeScheduledAction":{
      "Type":"AWS::AutoScaling::ScheduledAction",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "DesiredCapacity":"1",
        "StartTime":"2021-03-31T16:00:00Z"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-scheduledaction--examples--Scheduled_scaling_action_that_occurs_only_once--yaml"></a>

```
---
Resources:
  OneTimeScheduledAction:
    Type: AWS::AutoScaling::ScheduledAction
    Properties:
      AutoScalingGroupName: !Ref myASG
      DesiredCapacity: '1'
      StartTime: '2021-03-31T16:00:00Z'
```

## See also<a name="aws-resource-autoscaling-scheduledaction--seealso"></a>
+ [PutScheduledUpdateGroupAction](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutScheduledUpdateGroupAction.html) in the *Amazon EC2 Auto Scaling API Reference*
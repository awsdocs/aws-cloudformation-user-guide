# AWS::Scheduler::Schedule FlexibleTimeWindow<a name="aws-properties-scheduler-schedule-flexibletimewindow"></a>

Allows you to configure a time window during which EventBridge Scheduler invokes the schedule\.

## Syntax<a name="aws-properties-scheduler-schedule-flexibletimewindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-flexibletimewindow-syntax.json"></a>

```
{
  "[MaximumWindowInMinutes](#cfn-scheduler-schedule-flexibletimewindow-maximumwindowinminutes)" : Double,
  "[Mode](#cfn-scheduler-schedule-flexibletimewindow-mode)" : String
}
```

### YAML<a name="aws-properties-scheduler-schedule-flexibletimewindow-syntax.yaml"></a>

```
  [MaximumWindowInMinutes](#cfn-scheduler-schedule-flexibletimewindow-maximumwindowinminutes): Double
  [Mode](#cfn-scheduler-schedule-flexibletimewindow-mode): String
```

## Properties<a name="aws-properties-scheduler-schedule-flexibletimewindow-properties"></a>

`MaximumWindowInMinutes`  <a name="cfn-scheduler-schedule-flexibletimewindow-maximumwindowinminutes"></a>
The maximum time window during which a schedule can be invoked\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-scheduler-schedule-flexibletimewindow-mode"></a>
Determines whether the schedule is invoked within a flexible time window\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Synthetics::Canary Schedule<a name="aws-properties-synthetics-canary-schedule"></a>

This structure specifies how often a canary is to make runs and the date and time when it should stop making runs\.

## Syntax<a name="aws-properties-synthetics-canary-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-schedule-syntax.json"></a>

```
{
  "[DurationInSeconds](#cfn-synthetics-canary-schedule-durationinseconds)" : String,
  "[Expression](#cfn-synthetics-canary-schedule-expression)" : String
}
```

### YAML<a name="aws-properties-synthetics-canary-schedule-syntax.yaml"></a>

```
  [DurationInSeconds](#cfn-synthetics-canary-schedule-durationinseconds): String
  [Expression](#cfn-synthetics-canary-schedule-expression): String
```

## Properties<a name="aws-properties-synthetics-canary-schedule-properties"></a>

`DurationInSeconds`  <a name="cfn-synthetics-canary-schedule-durationinseconds"></a>
How long, in seconds, for the canary to continue making regular runs according to the schedule in the `Expression` value\. If you specify 0, the canary continues making runs until you stop it\. If you omit this field, the default of 0 is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-synthetics-canary-schedule-expression"></a>
A rate expression that defines how often the canary is to run\. The syntax is `rate(number unit)`\. *unit* can be `minute`, `minutes`, or `hour`\.   
For example, `rate(1 minute)` runs the canary once a minute, `rate(10 minutes)` runs it once every 10 minutes, and `rate(1 hour)` runs it once every hour\. You can specify a frequency between `rate(1 minute)` and `rate(1 hour)`\.  
Specifying `rate(0 minute)` or `rate(0 hour)` is a special value that causes the canary to run only once when it is started\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::ApplicationInsights::Application WindowsEvent<a name="aws-properties-applicationinsights-application-windowsevent"></a>

 The `AWS::ApplicationInsights::Application WindowsEvent` property type specifies a Windows Event to monitor for the component\.

## Syntax<a name="aws-properties-applicationinsights-application-windowsevent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-windowsevent-syntax.json"></a>

```
{
  "[EventLevels](#cfn-applicationinsights-application-windowsevent-eventlevels)" : [ String, ... ],
  "[EventName](#cfn-applicationinsights-application-windowsevent-eventname)" : String,
  "[LogGroupName](#cfn-applicationinsights-application-windowsevent-loggroupname)" : String,
  "[PatternSet](#cfn-applicationinsights-application-windowsevent-patternset)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-windowsevent-syntax.yaml"></a>

```
  [EventLevels](#cfn-applicationinsights-application-windowsevent-eventlevels): 
    - String
  [EventName](#cfn-applicationinsights-application-windowsevent-eventname): String
  [LogGroupName](#cfn-applicationinsights-application-windowsevent-loggroupname): String
  [PatternSet](#cfn-applicationinsights-application-windowsevent-patternset): String
```

## Properties<a name="aws-properties-applicationinsights-application-windowsevent-properties"></a>

`EventLevels`  <a name="cfn-applicationinsights-application-windowsevent-eventlevels"></a>
The levels of event to log\. You must specify each level to log\. Possible values include `INFORMATION`, `WARNING`, `ERROR`, `CRITICAL`, and `VERBOSE`\. This field is required for each type of Windows Event to log\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventName`  <a name="cfn-applicationinsights-application-windowsevent-eventname"></a>
The type of Windows Events to log, equivalent to the Windows Event log channel name\. For example, System, Security, CustomEventName, and so on\. This field is required for each type of Windows event to log\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroupName`  <a name="cfn-applicationinsights-application-windowsevent-loggroupname"></a>
The CloudWatch log group name to be associated with the monitored log\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternSet`  <a name="cfn-applicationinsights-application-windowsevent-patternset"></a>
The log pattern set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
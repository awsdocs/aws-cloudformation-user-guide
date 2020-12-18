# AWS::Pinpoint::ApplicationSettings Limits<a name="aws-properties-pinpoint-applicationsettings-limits"></a>

Specifies the default sending limits for campaigns in the application\. You can override these limits for a specific campaign\.

## Syntax<a name="aws-properties-pinpoint-applicationsettings-limits-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-applicationsettings-limits-syntax.json"></a>

```
{
  "[Daily](#cfn-pinpoint-applicationsettings-limits-daily)" : Integer,
  "[MaximumDuration](#cfn-pinpoint-applicationsettings-limits-maximumduration)" : Integer,
  "[MessagesPerSecond](#cfn-pinpoint-applicationsettings-limits-messagespersecond)" : Integer,
  "[Total](#cfn-pinpoint-applicationsettings-limits-total)" : Integer
}
```

### YAML<a name="aws-properties-pinpoint-applicationsettings-limits-syntax.yaml"></a>

```
  [Daily](#cfn-pinpoint-applicationsettings-limits-daily): Integer
  [MaximumDuration](#cfn-pinpoint-applicationsettings-limits-maximumduration): Integer
  [MessagesPerSecond](#cfn-pinpoint-applicationsettings-limits-messagespersecond): Integer
  [Total](#cfn-pinpoint-applicationsettings-limits-total): Integer
```

## Properties<a name="aws-properties-pinpoint-applicationsettings-limits-properties"></a>

`Daily`  <a name="cfn-pinpoint-applicationsettings-limits-daily"></a>
The maximum number of messages that a campaign can send to a single endpoint during a 24\-hour period\. The maximum value is 100\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumDuration`  <a name="cfn-pinpoint-applicationsettings-limits-maximumduration"></a>
The maximum amount of time, in seconds, that a campaign can attempt to deliver a message after the scheduled start time for the campaign\. The minimum value is 60 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessagesPerSecond`  <a name="cfn-pinpoint-applicationsettings-limits-messagespersecond"></a>
The maximum number of messages that a campaign can send each second\. The minimum value is 50\. The maximum value is 20,000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Total`  <a name="cfn-pinpoint-applicationsettings-limits-total"></a>
The maximum number of messages that a campaign can send to a single endpoint during the course of the campaign\. The maximum value is 100\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
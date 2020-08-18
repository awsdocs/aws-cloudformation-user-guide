# AWS::Pinpoint::Campaign WriteTreatmentResource<a name="aws-properties-pinpoint-campaign-writetreatmentresource"></a>

Specifies the settings for a campaign treatment\. A *treatment* is a variation of a campaign that's used for A/B testing of a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-writetreatmentresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-writetreatmentresource-syntax.json"></a>

```
{
  "[MessageConfiguration](#cfn-pinpoint-campaign-writetreatmentresource-messageconfiguration)" : MessageConfiguration,
  "[Schedule](#cfn-pinpoint-campaign-writetreatmentresource-schedule)" : Schedule,
  "[SizePercent](#cfn-pinpoint-campaign-writetreatmentresource-sizepercent)" : Integer,
  "[TreatmentDescription](#cfn-pinpoint-campaign-writetreatmentresource-treatmentdescription)" : String,
  "[TreatmentName](#cfn-pinpoint-campaign-writetreatmentresource-treatmentname)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-writetreatmentresource-syntax.yaml"></a>

```
  [MessageConfiguration](#cfn-pinpoint-campaign-writetreatmentresource-messageconfiguration): 
    MessageConfiguration
  [Schedule](#cfn-pinpoint-campaign-writetreatmentresource-schedule): 
    Schedule
  [SizePercent](#cfn-pinpoint-campaign-writetreatmentresource-sizepercent): Integer
  [TreatmentDescription](#cfn-pinpoint-campaign-writetreatmentresource-treatmentdescription): String
  [TreatmentName](#cfn-pinpoint-campaign-writetreatmentresource-treatmentname): String
```

## Properties<a name="aws-properties-pinpoint-campaign-writetreatmentresource-properties"></a>

`MessageConfiguration`  <a name="cfn-pinpoint-campaign-writetreatmentresource-messageconfiguration"></a>
The message configuration settings for the treatment\.  
*Required*: No  
*Type*: [MessageConfiguration](aws-properties-pinpoint-campaign-messageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-pinpoint-campaign-writetreatmentresource-schedule"></a>
The schedule settings for the treatment\.  
*Required*: No  
*Type*: [Schedule](aws-properties-pinpoint-campaign-schedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizePercent`  <a name="cfn-pinpoint-campaign-writetreatmentresource-sizepercent"></a>
The allocated percentage of users \(segment members\) to send the treatment to\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatmentDescription`  <a name="cfn-pinpoint-campaign-writetreatmentresource-treatmentdescription"></a>
A custom description of the treatment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatmentName`  <a name="cfn-pinpoint-campaign-writetreatmentresource-treatmentname"></a>
A custom name for the treatment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
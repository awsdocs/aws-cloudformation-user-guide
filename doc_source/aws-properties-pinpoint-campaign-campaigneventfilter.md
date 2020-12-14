# AWS::Pinpoint::Campaign CampaignEventFilter<a name="aws-properties-pinpoint-campaign-campaigneventfilter"></a>

Specifies the settings for events that cause a campaign to be sent\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaigneventfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaigneventfilter-syntax.json"></a>

```
{
  "[Dimensions](#cfn-pinpoint-campaign-campaigneventfilter-dimensions)" : EventDimensions,
  "[FilterType](#cfn-pinpoint-campaign-campaigneventfilter-filtertype)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaigneventfilter-syntax.yaml"></a>

```
  [Dimensions](#cfn-pinpoint-campaign-campaigneventfilter-dimensions): 
    EventDimensions
  [FilterType](#cfn-pinpoint-campaign-campaigneventfilter-filtertype): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaigneventfilter-properties"></a>

`Dimensions`  <a name="cfn-pinpoint-campaign-campaigneventfilter-dimensions"></a>
The dimension settings of the event filter for the campaign\.  
*Required*: No  
*Type*: [EventDimensions](aws-properties-pinpoint-campaign-eventdimensions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterType`  <a name="cfn-pinpoint-campaign-campaigneventfilter-filtertype"></a>
The type of event that causes the campaign to be sent\. Valid values are: `SYSTEM`, sends the campaign when a system event occurs; and, `ENDPOINT`, sends the campaign when an endpoint event occurs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
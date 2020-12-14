# AWS::Pinpoint::Campaign EventDimensions<a name="aws-properties-pinpoint-campaign-eventdimensions"></a>

Specifies the dimensions for an event filter that determines when a campaign is sent\.

## Syntax<a name="aws-properties-pinpoint-campaign-eventdimensions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-eventdimensions-syntax.json"></a>

```
{
  "[Attributes](#cfn-pinpoint-campaign-eventdimensions-attributes)" : Json,
  "[EventType](#cfn-pinpoint-campaign-eventdimensions-eventtype)" : SetDimension,
  "[Metrics](#cfn-pinpoint-campaign-eventdimensions-metrics)" : Json
}
```

### YAML<a name="aws-properties-pinpoint-campaign-eventdimensions-syntax.yaml"></a>

```
  [Attributes](#cfn-pinpoint-campaign-eventdimensions-attributes): Json
  [EventType](#cfn-pinpoint-campaign-eventdimensions-eventtype): 
    SetDimension
  [Metrics](#cfn-pinpoint-campaign-eventdimensions-metrics): Json
```

## Properties<a name="aws-properties-pinpoint-campaign-eventdimensions-properties"></a>

`Attributes`  <a name="cfn-pinpoint-campaign-eventdimensions-attributes"></a>
One or more custom attributes that your application reports to Amazon Pinpoint\. You can use these attributes as selection criteria when you create an event filter\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventType`  <a name="cfn-pinpoint-campaign-eventdimensions-eventtype"></a>
The name of the event that causes the campaign to be sent\. This can be a standard type of event that Amazon Pinpoint generates, such as `_email.delivered`, or a custom event that's specific to your application\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-campaign-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metrics`  <a name="cfn-pinpoint-campaign-eventdimensions-metrics"></a>
One or more custom metrics that your application reports to Amazon Pinpoint\. You can use these metrics as selection criteria when you create an event filter\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
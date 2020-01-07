# AWS::Pinpoint::Campaign<a name="aws-resource-pinpoint-campaign"></a>

Updates the settings for a campaign\.

## Syntax<a name="aws-resource-pinpoint-campaign-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-campaign-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::Campaign",
  "Properties" : {
      "[AdditionalTreatments](#cfn-pinpoint-campaign-additionaltreatments)" : [ [WriteTreatmentResource](aws-properties-pinpoint-campaign-writetreatmentresource.md), ... ],
      "[ApplicationId](#cfn-pinpoint-campaign-applicationid)" : String,
      "[CampaignHook](#cfn-pinpoint-campaign-campaignhook)" : [CampaignHook](aws-properties-pinpoint-campaign-campaignhook.md),
      "[Description](#cfn-pinpoint-campaign-description)" : String,
      "[HoldoutPercent](#cfn-pinpoint-campaign-holdoutpercent)" : Integer,
      "[IsPaused](#cfn-pinpoint-campaign-ispaused)" : Boolean,
      "[Limits](#cfn-pinpoint-campaign-limits)" : [Limits](aws-properties-pinpoint-campaign-limits.md),
      "[MessageConfiguration](#cfn-pinpoint-campaign-messageconfiguration)" : [MessageConfiguration](aws-properties-pinpoint-campaign-messageconfiguration.md),
      "[Name](#cfn-pinpoint-campaign-name)" : String,
      "[Schedule](#cfn-pinpoint-campaign-schedule)" : [Schedule](aws-properties-pinpoint-campaign-schedule.md),
      "[SegmentId](#cfn-pinpoint-campaign-segmentid)" : String,
      "[SegmentVersion](#cfn-pinpoint-campaign-segmentversion)" : Integer,
      "[Tags](#cfn-pinpoint-campaign-tags)" : Json,
      "[TreatmentDescription](#cfn-pinpoint-campaign-treatmentdescription)" : String,
      "[TreatmentName](#cfn-pinpoint-campaign-treatmentname)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-campaign-syntax.yaml"></a>

```
Type: AWS::Pinpoint::Campaign
Properties: 
  [AdditionalTreatments](#cfn-pinpoint-campaign-additionaltreatments): 
    - [WriteTreatmentResource](aws-properties-pinpoint-campaign-writetreatmentresource.md)
  [ApplicationId](#cfn-pinpoint-campaign-applicationid): String
  [CampaignHook](#cfn-pinpoint-campaign-campaignhook): 
    [CampaignHook](aws-properties-pinpoint-campaign-campaignhook.md)
  [Description](#cfn-pinpoint-campaign-description): String
  [HoldoutPercent](#cfn-pinpoint-campaign-holdoutpercent): Integer
  [IsPaused](#cfn-pinpoint-campaign-ispaused): Boolean
  [Limits](#cfn-pinpoint-campaign-limits): 
    [Limits](aws-properties-pinpoint-campaign-limits.md)
  [MessageConfiguration](#cfn-pinpoint-campaign-messageconfiguration): 
    [MessageConfiguration](aws-properties-pinpoint-campaign-messageconfiguration.md)
  [Name](#cfn-pinpoint-campaign-name): String
  [Schedule](#cfn-pinpoint-campaign-schedule): 
    [Schedule](aws-properties-pinpoint-campaign-schedule.md)
  [SegmentId](#cfn-pinpoint-campaign-segmentid): String
  [SegmentVersion](#cfn-pinpoint-campaign-segmentversion): Integer
  [Tags](#cfn-pinpoint-campaign-tags): Json
  [TreatmentDescription](#cfn-pinpoint-campaign-treatmentdescription): String
  [TreatmentName](#cfn-pinpoint-campaign-treatmentname): String
```

## Properties<a name="aws-resource-pinpoint-campaign-properties"></a>

`AdditionalTreatments`  <a name="cfn-pinpoint-campaign-additionaltreatments"></a>
An array of requests that defines additional treatments for the campaign, in addition to the default treatment for the campaign\.  
*Required*: No  
*Type*: List of [WriteTreatmentResource](aws-properties-pinpoint-campaign-writetreatmentresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationId`  <a name="cfn-pinpoint-campaign-applicationid"></a>
The unique ID of the Amazon Pinpoint app that the campaign is associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CampaignHook`  <a name="cfn-pinpoint-campaign-campaignhook"></a>
Specifies the AWS Lambda function to use as a code hook for a campaign\.  
*Required*: No  
*Type*: [CampaignHook](aws-properties-pinpoint-campaign-campaignhook.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-pinpoint-campaign-description"></a>
The custom description of the campaign\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HoldoutPercent`  <a name="cfn-pinpoint-campaign-holdoutpercent"></a>
The allocated percentage of users \(segment members\) who shouldn't receive messages from the campaign\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsPaused`  <a name="cfn-pinpoint-campaign-ispaused"></a>
Specifies whether to pause the campaign\. A paused campaign doesn't run unless you resume it by setting this value to `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limits`  <a name="cfn-pinpoint-campaign-limits"></a>
The messaging limits for the campaign\.  
*Required*: No  
*Type*: [Limits](aws-properties-pinpoint-campaign-limits.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageConfiguration`  <a name="cfn-pinpoint-campaign-messageconfiguration"></a>
The message configuration settings for the campaign\.  
*Required*: Yes  
*Type*: [MessageConfiguration](aws-properties-pinpoint-campaign-messageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-pinpoint-campaign-name"></a>
The name of the message template to use for the message\. If specified, this value must match the name of an existing message template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-pinpoint-campaign-schedule"></a>
The schedule settings for the campaign\.  
*Required*: Yes  
*Type*: [Schedule](aws-properties-pinpoint-campaign-schedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentId`  <a name="cfn-pinpoint-campaign-segmentid"></a>
The unique identifier for the segment to associate with the campaign\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentVersion`  <a name="cfn-pinpoint-campaign-segmentversion"></a>
The version of the segment to associate with the campaign\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pinpoint-campaign-tags"></a>
A string\-to\-string map of key\-value pairs that defines the tags to associate with the campaign\. Each tag consists of a required tag key and an associated tag value\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatmentDescription`  <a name="cfn-pinpoint-campaign-treatmentdescription"></a>
The custom description of a variation of the campaign to use for A/B testing\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatmentName`  <a name="cfn-pinpoint-campaign-treatmentname"></a>
The custom name of a variation of the campaign to use for A/B testing\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-campaign-return-values"></a>

### Ref<a name="aws-resource-pinpoint-campaign-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a string that combines the ID of the Amazon Pinpoint app with the ID of the segment that the campaign targets\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-campaign-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpoint-campaign-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the campaign\.

`CampaignId`  <a name="CampaignId-fn::getatt"></a>
The unique ID of the campaign\.
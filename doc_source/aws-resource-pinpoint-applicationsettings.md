# AWS::Pinpoint::ApplicationSettings<a name="aws-resource-pinpoint-applicationsettings"></a>

Specifies the settings for an Amazon Pinpoint app\.

In Amazon Pinpoint, an *app* \(also referred to as a *project*\) is a collection of settings, customer information, segments, and campaigns\.

## Syntax<a name="aws-resource-pinpoint-applicationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-applicationsettings-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::ApplicationSettings",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-applicationsettings-applicationid)" : String,
      "[CampaignHook](#cfn-pinpoint-applicationsettings-campaignhook)" : [CampaignHook](aws-properties-pinpoint-applicationsettings-campaignhook.md),
      "[CloudWatchMetricsEnabled](#cfn-pinpoint-applicationsettings-cloudwatchmetricsenabled)" : Boolean,
      "[Limits](#cfn-pinpoint-applicationsettings-limits)" : [Limits](aws-properties-pinpoint-applicationsettings-limits.md),
      "[QuietTime](#cfn-pinpoint-applicationsettings-quiettime)" : [QuietTime](aws-properties-pinpoint-applicationsettings-quiettime.md)
    }
}
```

### YAML<a name="aws-resource-pinpoint-applicationsettings-syntax.yaml"></a>

```
Type: AWS::Pinpoint::ApplicationSettings
Properties: 
  [ApplicationId](#cfn-pinpoint-applicationsettings-applicationid): String
  [CampaignHook](#cfn-pinpoint-applicationsettings-campaignhook): 
    [CampaignHook](aws-properties-pinpoint-applicationsettings-campaignhook.md)
  [CloudWatchMetricsEnabled](#cfn-pinpoint-applicationsettings-cloudwatchmetricsenabled): Boolean
  [Limits](#cfn-pinpoint-applicationsettings-limits): 
    [Limits](aws-properties-pinpoint-applicationsettings-limits.md)
  [QuietTime](#cfn-pinpoint-applicationsettings-quiettime): 
    [QuietTime](aws-properties-pinpoint-applicationsettings-quiettime.md)
```

## Properties<a name="aws-resource-pinpoint-applicationsettings-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-applicationsettings-applicationid"></a>
The unique ID of the Amazon Pinpoint app\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CampaignHook`  <a name="cfn-pinpoint-applicationsettings-campaignhook"></a>
The settings for the AWS Lambda function to use by default as a code hook for campaigns in the application\. To override these settings for a specific campaign, use the Campaign resource to define custom Lambda function settings for the campaign\.  
*Required*: No  
*Type*: [CampaignHook](aws-properties-pinpoint-applicationsettings-campaignhook.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchMetricsEnabled`  <a name="cfn-pinpoint-applicationsettings-cloudwatchmetricsenabled"></a>
Specifies whether to enable application\-related alarms in Amazon CloudWatch\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limits`  <a name="cfn-pinpoint-applicationsettings-limits"></a>
The default sending limits for campaigns in the application\. To override these limits for a specific campaign, use the Campaign resource to define custom limits for the campaign\.  
*Required*: No  
*Type*: [Limits](aws-properties-pinpoint-applicationsettings-limits.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuietTime`  <a name="cfn-pinpoint-applicationsettings-quiettime"></a>
The default quiet time for campaigns in the application\. Quiet time is a specific time range when campaigns don't send messages to endpoints, if all the following conditions are met:  
\- The `EndpointDemographic.Timezone` property of the endpoint is set to a valid value\.  
\- The current time in the endpoint's time zone is later than or equal to the time specified by the `QuietTime.Start` property for the application \(or a campaign that has custom quiet time settings\)\.  
\- The current time in the endpoint's time zone is earlier than or equal to the time specified by the `QuietTime.End` property for the application \(or a campaign that has custom quiet time settings\)\.  
If any of the preceding conditions isn't met, the endpoint will receive messages from a campaign, even if quiet time is enabled\.  
To override the default quiet time settings for a specific campaign, use the Campaign resource to define a custom quiet time for the campaign\.  
*Required*: No  
*Type*: [QuietTime](aws-properties-pinpoint-applicationsettings-quiettime.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-applicationsettings-return-values"></a>

### Ref<a name="aws-resource-pinpoint-applicationsettings-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Amazon Pinpoint app that you're specifying the settings for\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.
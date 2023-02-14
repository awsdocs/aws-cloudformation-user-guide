# AWS::Pinpoint::ApplicationSettings CampaignHook<a name="aws-properties-pinpoint-applicationsettings-campaignhook"></a>

Specifies the Lambda function to use by default as a code hook for campaigns in the application\.

## Syntax<a name="aws-properties-pinpoint-applicationsettings-campaignhook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-applicationsettings-campaignhook-syntax.json"></a>

```
{
  "[LambdaFunctionName](#cfn-pinpoint-applicationsettings-campaignhook-lambdafunctionname)" : String,
  "[Mode](#cfn-pinpoint-applicationsettings-campaignhook-mode)" : String,
  "[WebUrl](#cfn-pinpoint-applicationsettings-campaignhook-weburl)" : String
}
```

### YAML<a name="aws-properties-pinpoint-applicationsettings-campaignhook-syntax.yaml"></a>

```
  [LambdaFunctionName](#cfn-pinpoint-applicationsettings-campaignhook-lambdafunctionname): String
  [Mode](#cfn-pinpoint-applicationsettings-campaignhook-mode): String
  [WebUrl](#cfn-pinpoint-applicationsettings-campaignhook-weburl): String
```

## Properties<a name="aws-properties-pinpoint-applicationsettings-campaignhook-properties"></a>

`LambdaFunctionName`  <a name="cfn-pinpoint-applicationsettings-campaignhook-lambdafunctionname"></a>
The name or Amazon Resource Name \(ARN\) of the Lambda function that Amazon Pinpoint invokes to send messages for campaigns in the application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-pinpoint-applicationsettings-campaignhook-mode"></a>
The mode that Amazon Pinpoint uses to invoke the Lambda function\. Possible values are:  
+  `FILTER` \- Invoke the function to customize the segment that's used by a campaign\.
+  `DELIVERY` \- \(Deprecated\) Previously, invoked the function to send a campaign through a custom channel\. This functionality is not supported anymore\. To send a campaign through a custom channel, use the `CustomDeliveryConfiguration` and `CampaignCustomMessage` objects of the campaign\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebUrl`  <a name="cfn-pinpoint-applicationsettings-campaignhook-weburl"></a>
The web URL that Amazon Pinpoint calls to invoke the Lambda function over HTTPS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
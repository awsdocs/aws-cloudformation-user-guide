# AWS::Pinpoint::Campaign CampaignHook<a name="aws-properties-pinpoint-campaign-campaignhook"></a>

Specifies settings for invoking an AWS Lambda function that customizes a segment for a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaignhook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaignhook-syntax.json"></a>

```
{
  "[LambdaFunctionName](#cfn-pinpoint-campaign-campaignhook-lambdafunctionname)" : String,
  "[Mode](#cfn-pinpoint-campaign-campaignhook-mode)" : String,
  "[WebUrl](#cfn-pinpoint-campaign-campaignhook-weburl)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaignhook-syntax.yaml"></a>

```
  [LambdaFunctionName](#cfn-pinpoint-campaign-campaignhook-lambdafunctionname): String
  [Mode](#cfn-pinpoint-campaign-campaignhook-mode): String
  [WebUrl](#cfn-pinpoint-campaign-campaignhook-weburl): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaignhook-properties"></a>

`LambdaFunctionName`  <a name="cfn-pinpoint-campaign-campaignhook-lambdafunctionname"></a>
The name or Amazon Resource Name \(ARN\) of the AWS Lambda function that Amazon Pinpoint invokes to customize a segment for a campaign\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-pinpoint-campaign-campaignhook-mode"></a>
The mode that Amazon Pinpoint uses to invoke the AWS Lambda function\. Possible values are:  
+  `FILTER` \- Invoke the function to customize the segment that's used by a campaign\.
+  `DELIVERY` \- \(Deprecated\) Previously, invoked the function to send a campaign through a custom channel\. This functionality is not supported anymore\. To send a campaign through a custom channel, use the `CustomDeliveryConfiguration` and `CampaignCustomMessage` objects of the campaign\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebUrl`  <a name="cfn-pinpoint-campaign-campaignhook-weburl"></a>
The web URL that Amazon Pinpoint calls to invoke the AWS Lambda function over HTTPS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
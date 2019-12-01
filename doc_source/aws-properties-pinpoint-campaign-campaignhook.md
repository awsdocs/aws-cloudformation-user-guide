# AWS::Pinpoint::Campaign CampaignHook<a name="aws-properties-pinpoint-campaign-campaignhook"></a>

Specifies the AWS Lambda function to use as a code hook for a campaign\.

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
The name or Amazon Resource Name \(ARN\) of the AWS Lambda function that Amazon Pinpoint invokes to send messages for a campaign\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-pinpoint-campaign-campaignhook-mode"></a>
Specifies which Lambda mode to use when invoking the AWS Lambda function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebUrl`  <a name="cfn-pinpoint-campaign-campaignhook-weburl"></a>
The web URL that Amazon Pinpoint calls to invoke the AWS Lambda function over HTTPS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
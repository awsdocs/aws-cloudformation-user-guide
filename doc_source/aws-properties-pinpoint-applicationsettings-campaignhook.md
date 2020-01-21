# AWS::Pinpoint::ApplicationSettings CampaignHook<a name="aws-properties-pinpoint-applicationsettings-campaignhook"></a>

Specifies the AWS Lambda function to use by default as a code hook for campaigns in the application\.

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
The name or Amazon Resource Name \(ARN\) of the AWS Lambda function that Amazon Pinpoint invokes to send messages for campaigns in the application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-pinpoint-applicationsettings-campaignhook-mode"></a>
Specifies which Lambda mode to use when invoking the AWS Lambda function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebUrl`  <a name="cfn-pinpoint-applicationsettings-campaignhook-weburl"></a>
The web URL that Amazon Pinpoint calls to invoke the AWS Lambda function over HTTPS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
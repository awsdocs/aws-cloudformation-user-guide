# AWS::CodePipeline::Webhook WebhookFilterRule<a name="aws-properties-codepipeline-webhook-webhookfilterrule"></a>

The event criteria that specify when a webhook notification is sent to your URL\.

## Syntax<a name="aws-properties-codepipeline-webhook-webhookfilterrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-webhook-webhookfilterrule-syntax.json"></a>

```
{
  "[JsonPath](#cfn-codepipeline-webhook-webhookfilterrule-jsonpath)" : String,
  "[MatchEquals](#cfn-codepipeline-webhook-webhookfilterrule-matchequals)" : String
}
```

### YAML<a name="aws-properties-codepipeline-webhook-webhookfilterrule-syntax.yaml"></a>

```
  [JsonPath](#cfn-codepipeline-webhook-webhookfilterrule-jsonpath): String
  [MatchEquals](#cfn-codepipeline-webhook-webhookfilterrule-matchequals): String
```

## Properties<a name="aws-properties-codepipeline-webhook-webhookfilterrule-properties"></a>

`JsonPath`  <a name="cfn-codepipeline-webhook-webhookfilterrule-jsonpath"></a>
A JsonPath expression that is applied to the body/payload of the webhook\. The value selected by the JsonPath expression must match the value specified in the `MatchEquals` field\. Otherwise, the request is ignored\. For more information, see [Java JsonPath implementation](https://github.com/json-path/JsonPath) in GitHub\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchEquals`  <a name="cfn-codepipeline-webhook-webhookfilterrule-matchequals"></a>
The value selected by the `JsonPath` expression must match what is supplied in the `MatchEquals` field\. Otherwise, the request is ignored\. Properties from the target action configuration can be included as placeholders in this value by surrounding the action configuration key with curly brackets\. For example, if the value supplied here is "refs/heads/\{Branch\}" and the target action has an action configuration property called "Branch" with a value of "master", the `MatchEquals` value is evaluated as "refs/heads/master"\. For a list of action configuration properties for built\-in action types, see [Pipeline Structure Reference Action Requirements](https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#action-requirements)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
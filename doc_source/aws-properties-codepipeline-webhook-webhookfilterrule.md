# AWS CodePipeline Webhook WebhookFilterRule<a name="aws-properties-codepipeline-webhook-webhookfilterrule"></a>

<a name="aws-properties-codepipeline-webhook-webhookfilterrule-description"></a>The `WebhookFilterRule` property type specifies events that will trigger a webhook\. For more information, see [Webhook Definition](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_WebhookDefinition.html) in the *AWS CodePipeline API Reference*\.

<a name="aws-properties-codepipeline-webhook-webhookfilterrule-inheritance"></a> The `Filters` property of the [AWS::CodePipeline::Webhook](aws-resource-codepipeline-webhook.md) resource contains a list of `WebhookFilterRule` property types\. The is the list of rules applied to the body/payload sent in the POST request to a webhook URL\.

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
A JsonPath expression that will be applied to the body/payload of the webhook\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MatchEquals`  <a name="cfn-codepipeline-webhook-webhookfilterrule-matchequals"></a>
The value selected by the JsonPath expression must match what is supplied in the MatchEquals field, otherwise the request will be ignored\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
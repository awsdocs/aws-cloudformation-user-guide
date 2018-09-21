# AWS CodePipeline Webhook WebhookAuthConfiguration<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration"></a>

<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration-description"></a>The `WebhookAuthConfiguration` property type configures the authentication applied to incoming webhook trigger requests\. For more information, see [Webhook Definition](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_WebhookDefinition.html) in the *AWS CodePipeline API Reference*\.

<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration-inheritance"></a> `WebhookAuthConfiguration` is the property type of the `AuthenticationConfiguration` property of the [AWS::CodePipeline::Webhook](aws-resource-codepipeline-webhook.md) resource\.

## Syntax<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration-syntax.json"></a>

```
{
  "[AllowedIPRange](#cfn-codepipeline-webhook-webhookauthconfiguration-allowediprange)" : String,
  "[SecretToken](#cfn-codepipeline-webhook-webhookauthconfiguration-secrettoken)" : String
}
```

### YAML<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration-syntax.yaml"></a>

```
[AllowedIPRange](#cfn-codepipeline-webhook-webhookauthconfiguration-allowediprange): String
[SecretToken](#cfn-codepipeline-webhook-webhookauthconfiguration-secrettoken): String
```

## Properties<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration-properties"></a>

`AllowedIPRange`  <a name="cfn-codepipeline-webhook-webhookauthconfiguration-allowediprange"></a>
The property used to configure acceptance of webhooks within a specific IP range\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecretToken`  <a name="cfn-codepipeline-webhook-webhookauthconfiguration-secrettoken"></a>
The property used to configure GitHub authentication\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
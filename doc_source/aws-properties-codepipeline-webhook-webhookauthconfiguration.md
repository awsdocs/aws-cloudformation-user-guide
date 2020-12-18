# AWS::CodePipeline::Webhook WebhookAuthConfiguration<a name="aws-properties-codepipeline-webhook-webhookauthconfiguration"></a>

The authentication applied to incoming webhook trigger requests\.

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
The property used to configure acceptance of webhooks in an IP address range\. For IP, only the `AllowedIPRange` property must be set\. This property must be set to a valid CIDR range\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretToken`  <a name="cfn-codepipeline-webhook-webhookauthconfiguration-secrettoken"></a>
The property used to configure GitHub authentication\. For GITHUB\_HMAC, only the `SecretToken` property must be set\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
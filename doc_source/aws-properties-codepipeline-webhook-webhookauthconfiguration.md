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
The property used to configure acceptance of webhooks within a specific IP range\. For IP, only the `AllowedIPRange` property must be set, and this property must be set to a valid CIDR range\.  
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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`

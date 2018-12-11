# AWS::CodePipeline::Webhook<a name="aws-resource-codepipeline-webhook"></a>

The `AWS::CodePipeline::Webhook` resource creates and registers your webhook\. After the webhook is created and registered, it triggers your pipeline to start every time an external event occurs\. For more information, see [Configure Your GitHub Pipelines to Use Webhooks for Change Detection](https://docs.aws.amazon.com/codepipeline/latest/userguide/pipelines-webhooks-migration.html) in the *AWS CodePipeline User Guide*\.

## Syntax<a name="aws-resource-codepipeline-webhook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codepipeline-webhook-syntax.json"></a>

```
{
  "Type" : "AWS::CodePipeline::Webhook",
  "Properties" : {
    "[AuthenticationConfiguration](#cfn-codepipeline-webhook-authenticationconfiguration)" : [*WebhookAuthConfiguration*](aws-properties-codepipeline-webhook-webhookauthconfiguration.md),
    "[Filters](#cfn-codepipeline-webhook-filters)" : [ [*WebhookFilterRule*](aws-properties-codepipeline-webhook-webhookfilterrule.md), ... ],
    "[Authentication](#cfn-codepipeline-webhook-authentication)" : String,
    "[TargetPipeline](#cfn-codepipeline-webhook-targetpipeline)" : String,
    "[TargetAction](#cfn-codepipeline-webhook-targetaction)" : String,
    "[Name](#cfn-codepipeline-webhook-name)" : String,
    "[TargetPipelineVersion](#cfn-codepipeline-webhook-targetpipelineversion)" : Integer,
    "[RegisterWithThirdParty](#cfn-codepipeline-webhook-registerwiththirdparty)" : Boolean
  }
}
```

### YAML<a name="aws-resource-codepipeline-webhook-syntax.yaml"></a>

```
Type: "AWS::CodePipeline::Webhook"
Properties:
  [AuthenticationConfiguration](#cfn-codepipeline-webhook-authenticationconfiguration):
    [*WebhookAuthConfiguration*](aws-properties-codepipeline-webhook-webhookauthconfiguration.md)
  [Filters](#cfn-codepipeline-webhook-filters): 
    - [*WebhookFilterRule*](aws-properties-codepipeline-webhook-webhookfilterrule.md)
  [Authentication](#cfn-codepipeline-webhook-authentication): String
  [TargetPipeline](#cfn-codepipeline-webhook-targetpipeline): String
  [TargetAction](#cfn-codepipeline-webhook-targetaction): String
  [Name](#cfn-codepipeline-webhook-name): String
  [TargetPipelineVersion](#cfn-codepipeline-webhook-targetpipelineversion): Integer
  [RegisterWithThirdParty](#cfn-codepipeline-webhook-registerwiththirdparty): Boolean
```

## Properties<a name="aws-resource-codepipeline-webhook-properties"></a>

`Authentication`  <a name="cfn-codepipeline-webhook-authentication"></a>
The type of authentication scheme that allows the trigger request to be accepted\. For more information, see [Webhook Definition](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_WebhookDefinition.html) in the *AWS CodePipeline API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AuthenticationConfiguration`  <a name="cfn-codepipeline-webhook-authenticationconfiguration"></a>
Properties that configure the authentication applied to incoming webhook trigger requests\. For more information, see [Webhook Definition](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_WebhookDefinition.html) in the *AWS CodePipeline API Reference*\.  
 *Required*: Yes  
 *Type*: [WebhookAuthConfiguration](aws-properties-codepipeline-webhook-webhookauthconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Filters`  <a name="cfn-codepipeline-webhook-filters"></a>
A list of rules applied to the body/payload sent in the POST request to a webhook URL\. All defined rules must pass for the request to be accepted and the pipeline started\.  
 *Required*: Yes  
 *Type*: List of [WebhookFilterRule](aws-properties-codepipeline-webhook-webhookfilterrule.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-codepipeline-webhook-name"></a>
The name of the webhook to be created and, if applicable, to register with a supported third party\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RegisterWithThirdParty`  <a name="cfn-codepipeline-webhook-registerwiththirdparty"></a>
Indicates whether to register the webhook with a third party\. Third party registration configures a connection between the webhook that was created and the external tool, such as GitHub, with events to be detected\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetAction`  <a name="cfn-codepipeline-webhook-targetaction"></a>
The name of the action in a pipeline you want to connect to the webhook\. The action must be from the source \(first\) stage of the pipeline\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetPipeline`  <a name="cfn-codepipeline-webhook-targetpipeline"></a>
The name of the pipeline you want to connect to the webhook\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetPipelineVersion`  <a name="cfn-codepipeline-webhook-targetpipelineversion"></a>
The version number of the pipeline to be connected to the trigger request\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-codepipeline-webhook-returnvalues"></a>

### Ref<a name="aws-resource-codepipeline-webhook-ref"></a>

When you pass the logical ID of an `AWS::CodePipeline::Webhook` resource to the intrinsic `Ref` function, the function returns the webhook name, such as `MyFirstPipeline-SourceAction1-Webhook-utb9LrOl24Kk`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-codepipeline-webhook-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Url`  
The webhook URL generated by AWS CodePipeline, such as `https://eu-central-1.webhooks.aws/trigger123456`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Example<a name="aws-resource-codepipeline-webhook-example1"></a>

The following example creates a webhook named `MyWebhook` and registers the webhook for the pipeline's GitHub source repository\. In this example, `WebhookPipeline` is the logical ID of the pipeline to which you want to add the webhook\.

### JSON<a name="aws-resource-codepipeline-webhook-example1.json"></a>

```
{
    "Webhook": {
        "Type": "AWS::CodePipeline::Webhook",
        "Properties": {
            "AuthenticationConfiguration": {
                "SecretToken": "secret"
            },
            "Filters": [
                {
                    "JsonPath": "$.ref",
                    "MatchEquals": "refs/heads/{Branch}"
                }
            ],
            "Authentication": "GITHUB_HMAC",
            "TargetPipeline": { "Ref" : "WebhookPipeline" },
            "TargetAction": "Source",
            "Name": "MyWebhook",
            "TargetPipelineVersion": { "Fn::GetAtt" : [ "WebhookPipeline", "Version" ] },
            "RegisterWithThirdParty": "true"
        }
    }
}
```

### YAML<a name="aws-resource-codepipeline-webhook-example1.yaml"></a>

```
Webhook:
  Type: 'AWS::CodePipeline::Webhook'
  Properties:
    AuthenticationConfiguration:
      SecretToken: secret
    Filters:
    - JsonPath: "$.ref"
      MatchEquals: refs/heads/{Branch}
    Authentication: GITHUB_HMAC
    TargetPipeline: !Ref WebhookPipeline
    TargetAction: Source
    Name: MyWebhook
    TargetPipelineVersion: !GetAtt WebhookPipeline.Version
    RegisterWithThirdParty: 'true'
```
# AWS::CodePipeline::Webhook<a name="aws-resource-codepipeline-webhook"></a>

The `AWS::CodePipeline::Webhook` resource creates and registers your webhook\. After the webhook is created and registered, it triggers your pipeline to start every time an external event occurs\. For more information, see [Configure Your GitHub Pipelines to Use Webhooks for Change Detection](https://docs.aws.amazon.com/codepipeline/latest/userguide/pipelines-webhooks-migration.html) in the *AWS CodePipeline User Guide*\.

We strongly recommend that you use AWS Secrets Manager to store your credentials\. If you use Secrets Manager, you must have already configured and stored your secret parameters in Secrets Manager\. For more information, see [ Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager)\. 

**Important**  
When passing secret parameters, do not enter the value directly into the template\. The value is rendered as plaintext and is therefore readable\. For security reasons, do not use plaintext in your AWS CloudFormation template to store your credentials\.

## Syntax<a name="aws-resource-codepipeline-webhook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codepipeline-webhook-syntax.json"></a>

```
{
  "Type" : "AWS::CodePipeline::Webhook",
  "Properties" : {
      "[Authentication](#cfn-codepipeline-webhook-authentication)" : String,
      "[AuthenticationConfiguration](#cfn-codepipeline-webhook-authenticationconfiguration)" : WebhookAuthConfiguration,
      "[Filters](#cfn-codepipeline-webhook-filters)" : [ WebhookFilterRule, ... ],
      "[Name](#cfn-codepipeline-webhook-name)" : String,
      "[RegisterWithThirdParty](#cfn-codepipeline-webhook-registerwiththirdparty)" : Boolean,
      "[TargetAction](#cfn-codepipeline-webhook-targetaction)" : String,
      "[TargetPipeline](#cfn-codepipeline-webhook-targetpipeline)" : String,
      "[TargetPipelineVersion](#cfn-codepipeline-webhook-targetpipelineversion)" : Integer
    }
}
```

### YAML<a name="aws-resource-codepipeline-webhook-syntax.yaml"></a>

```
Type: AWS::CodePipeline::Webhook
Properties: 
  [Authentication](#cfn-codepipeline-webhook-authentication): String
  [AuthenticationConfiguration](#cfn-codepipeline-webhook-authenticationconfiguration): 
    WebhookAuthConfiguration
  [Filters](#cfn-codepipeline-webhook-filters): 
    - WebhookFilterRule
  [Name](#cfn-codepipeline-webhook-name): String
  [RegisterWithThirdParty](#cfn-codepipeline-webhook-registerwiththirdparty): Boolean
  [TargetAction](#cfn-codepipeline-webhook-targetaction): String
  [TargetPipeline](#cfn-codepipeline-webhook-targetpipeline): String
  [TargetPipelineVersion](#cfn-codepipeline-webhook-targetpipelineversion): Integer
```

## Properties<a name="aws-resource-codepipeline-webhook-properties"></a>

`Authentication`  <a name="cfn-codepipeline-webhook-authentication"></a>
Supported options are GITHUB\_HMAC, IP, and UNAUTHENTICATED\.  
+ For information about the authentication scheme implemented by GITHUB\_HMAC, see [Securing your webhooks](https://developer.github.com/webhooks/securing/) on the GitHub Developer website\.
+  IP rejects webhooks trigger requests unless they originate from an IP address in the IP range whitelisted in the authentication configuration\.
+  UNAUTHENTICATED accepts all webhook trigger requests regardless of origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `GITHUB_HMAC | IP | UNAUTHENTICATED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthenticationConfiguration`  <a name="cfn-codepipeline-webhook-authenticationconfiguration"></a>
Properties that configure the authentication applied to incoming webhook trigger requests\. The required properties depend on the authentication type\. For GITHUB\_HMAC, only the `SecretToken `property must be set\. For IP, only the `AllowedIPRange `property must be set to a valid CIDR range\. For UNAUTHENTICATED, no properties can be set\.  
*Required*: Yes  
*Type*: [WebhookAuthConfiguration](aws-properties-codepipeline-webhook-webhookauthconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filters`  <a name="cfn-codepipeline-webhook-filters"></a>
A list of rules applied to the body/payload sent in the POST request to a webhook URL\. All defined rules must pass for the request to be accepted and the pipeline started\.  
*Required*: Yes  
*Type*: List of [WebhookFilterRule](aws-properties-codepipeline-webhook-webhookfilterrule.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codepipeline-webhook-name"></a>
The name of the webhook\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9.@\-_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegisterWithThirdParty`  <a name="cfn-codepipeline-webhook-registerwiththirdparty"></a>
Configures a connection between the webhook that was created and the external tool with events to be detected\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetAction`  <a name="cfn-codepipeline-webhook-targetaction"></a>
The name of the action in a pipeline you want to connect to the webhook\. The action must be from the source \(first\) stage of the pipeline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9.@\-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetPipeline`  <a name="cfn-codepipeline-webhook-targetpipeline"></a>
The name of the pipeline you want to connect to the webhook\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9.@\-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetPipelineVersion`  <a name="cfn-codepipeline-webhook-targetpipelineversion"></a>
The version number of the pipeline to be connected to the trigger request\.  
Required: Yes   
Type: Integer   
 Update requires: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-codepipeline-webhook-return-values"></a>

### Ref<a name="aws-resource-codepipeline-webhook-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the webhook name, such as MyFirstPipeline\-SourceAction1\-Webhook\-utb9LrOl24Kk\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codepipeline-webhook-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codepipeline-webhook-return-values-fn--getatt-fn--getatt"></a>

`Url`  <a name="Url-fn::getatt"></a>
The webhook URL generated by AWS CodePipeline, such as https://eu\-central\-1\.webhooks\.aws/trigger123456\.

## Examples<a name="aws-resource-codepipeline-webhook--examples"></a>



### Webhook Resource Configuration<a name="aws-resource-codepipeline-webhook--examples--Webhook_Resource_Configuration"></a>

The following example creates a webhook named MyWebhook and registers the webhook for the pipeline's GitHub source repository\. In this example, WebhookPipeline is the logical ID of the pipeline to which you want to add the webhook\.

We strongly recommend that you use AWS Secrets Manager to store your credentials\. If you use Secrets Manager, you must have already configured and stored your secret parameters in Secrets Manager\. This example uses dynamic references to AWS Secrets Manager for the GitHub credentials for your webhook, in the form of the `{{resolve:secretsmanager:MyGitHubSecret:SecretString:token}}` reference\. For more information, see [ Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager)\. 

**Important**  
When passing secret parameters, do not enter the value directly into the template\. The value is rendered as plaintext and is therefore readable\. For security reasons, do not use plaintext in your AWS CloudFormation template to store your credentials\.

#### JSON<a name="aws-resource-codepipeline-webhook--examples--Webhook_Resource_Configuration--json"></a>

```
{ 
  "Webhook": { 
    "Type": "AWS::CodePipeline::Webhook", 
    "Properties": {
      "AuthenticationConfiguration": { 
        "SecretToken": "{{resolve:secretsmanager:MyGitHubSecret:SecretString:token}}" 
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

#### YAML<a name="aws-resource-codepipeline-webhook--examples--Webhook_Resource_Configuration--yaml"></a>

```
Webhook: 
  Type: 'AWS::CodePipeline::Webhook' 
  Properties:
    AuthenticationConfiguration: 
      SecretToken: {{resolve:secretsmanager:MyGitHubSecret:SecretString:token}} 
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
# AWS CodePipeline CustomActionType Settings<a name="aws-resource-codepipeline-customactiontype-settings"></a>

`Settings` is a property of the [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) resource that provides URLs that users can access to view information about the AWS CodePipeline custom action\.

## Syntax<a name="w3ab2c21c14d444b5"></a>

### JSON<a name="aws-properties-codepipeline-customactiontype-settings-syntax.json"></a>

```
{
  "[EntityUrlTemplate](#cfn-codepipeline-customactiontype-settings-entityurltemplate)" : String,
  "[ExecutionUrlTemplate](#cfn-codepipeline-customactiontype-settings-executionurltemplate)" : String,
  "[RevisionUrlTemplate](#cfn-codepipeline-customactiontype-settings-revisionurltemplate)" : String,
  "[ThirdPartyConfigurationUrl](#cfn-codepipeline-customactiontype-settings-thirdpartyconfigurationurl)" : String
}
```

### YAML<a name="aws-properties-codepipeline-customactiontype-settings-syntax.yaml"></a>

```
[EntityUrlTemplate](#cfn-codepipeline-customactiontype-settings-entityurltemplate): String
[ExecutionUrlTemplate](#cfn-codepipeline-customactiontype-settings-executionurltemplate): String
[RevisionUrlTemplate](#cfn-codepipeline-customactiontype-settings-revisionurltemplate): String
[ThirdPartyConfigurationUrl](#cfn-codepipeline-customactiontype-settings-thirdpartyconfigurationurl): String
```

## Properties<a name="w3ab2c21c14d444b7"></a>

`EntityUrlTemplate`  <a name="cfn-codepipeline-customactiontype-settings-entityurltemplate"></a>
The URL that is returned to the AWS CodePipeline console that links to the resources of the external system, such as the configuration page for an AWS CodeDeploy deployment group\.  
*Required*: No  
*Type*: String

`ExecutionUrlTemplate`  <a name="cfn-codepipeline-customactiontype-settings-executionurltemplate"></a>
The URL that is returned to the AWS CodePipeline console that links to the top\-level landing page for the external system, such as the console page for AWS CodeDeploy\.  
*Required*: No  
*Type*: String

`RevisionUrlTemplate`  <a name="cfn-codepipeline-customactiontype-settings-revisionurltemplate"></a>
The URL that is returned to the AWS CodePipeline console that links to the page where customers can update or change the configuration of the external action\.  
*Required*: No  
*Type*: String

`ThirdPartyConfigurationUrl`  <a name="cfn-codepipeline-customactiontype-settings-thirdpartyconfigurationurl"></a>
The URL of a sign\-up page where users can sign up for an external service and specify the initial configurations for the service's action\.  
*Required*: No  
*Type*: String
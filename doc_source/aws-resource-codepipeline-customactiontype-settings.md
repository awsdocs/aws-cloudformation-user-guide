# AWS CodePipeline CustomActionType Settings<a name="aws-resource-codepipeline-customactiontype-settings"></a>

`Settings` is a property of the [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) resource that provides URLs that users can access to view information about the AWS CodePipeline custom action\.

## Syntax<a name="w3ab2c21c14d370b5"></a>

### JSON<a name="aws-properties-codepipeline-customactiontype-settings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-entityurltemplate)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-executionurltemplate)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-revisionurltemplate)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-thirdpartyconfigurationurl)" : String
}
```

### YAML<a name="aws-properties-codepipeline-customactiontype-settings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-entityurltemplate): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-executionurltemplate): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-revisionurltemplate): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-settings-thirdpartyconfigurationurl): String
```

## Properties<a name="w3ab2c21c14d370b7"></a>

`EntityUrlTemplate`  
The URL that is returned to the AWS CodePipeline console that links to the resources of the external system, such as the configuration page for an AWS CodeDeploy deployment group\.  
*Required: *No  
*Type*: String

`ExecutionUrlTemplate`  
The URL that is returned to the AWS CodePipeline console that links to the top\-level landing page for the external system, such as the console page for AWS CodeDeploy\.  
*Required: *No  
*Type*: String

`RevisionUrlTemplate`  
The URL that is returned to the AWS CodePipeline console that links to the page where customers can update or change the configuration of the external action\.  
*Required: *No  
*Type*: String

`ThirdPartyConfigurationUrl`  
The URL of a sign\-up page where users can sign up for an external service and specify the initial configurations for the service's action\.  
*Required: *No  
*Type*: String
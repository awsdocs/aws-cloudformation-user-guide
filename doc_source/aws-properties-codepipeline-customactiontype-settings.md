# AWS::CodePipeline::CustomActionType Settings<a name="aws-properties-codepipeline-customactiontype-settings"></a>

 `Settings` is a property of the `AWS::CodePipeline::CustomActionType` resource that provides URLs that users can access to view information about the CodePipeline custom action\.

## Syntax<a name="aws-properties-codepipeline-customactiontype-settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-codepipeline-customactiontype-settings-properties"></a>

`EntityUrlTemplate`  <a name="cfn-codepipeline-customactiontype-settings-entityurltemplate"></a>
The URL returned to the AWS CodePipeline console that provides a deep link to the resources of the external system, such as the configuration page for an AWS CodeDeploy deployment group\. This link is provided as part of the action display in the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionUrlTemplate`  <a name="cfn-codepipeline-customactiontype-settings-executionurltemplate"></a>
The URL returned to the AWS CodePipeline console that contains a link to the top\-level landing page for the external system, such as the console page for AWS CodeDeploy\. This link is shown on the pipeline view page in the AWS CodePipeline console and provides a link to the execution entity of the external action\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RevisionUrlTemplate`  <a name="cfn-codepipeline-customactiontype-settings-revisionurltemplate"></a>
The URL returned to the AWS CodePipeline console that contains a link to the page where customers can update or change the configuration of the external action\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThirdPartyConfigurationUrl`  <a name="cfn-codepipeline-customactiontype-settings-thirdpartyconfigurationurl"></a>
The URL of a sign\-up page where users can sign up for an external service and perform initial configuration of the action provided by that service\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
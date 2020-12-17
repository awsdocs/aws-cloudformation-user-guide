# AWS::CodePipeline::Pipeline ActionTypeId<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid"></a>

Represents information about an action type\.

## Syntax<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid-syntax.json"></a>

```
{
  "[Category](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-category)" : String,
  "[Owner](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-owner)" : String,
  "[Provider](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-provider)" : String,
  "[Version](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-version)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid-syntax.yaml"></a>

```
  [Category](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-category): String
  [Owner](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-owner): String
  [Provider](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-provider): String
  [Version](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-version): String
```

## Properties<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid-properties"></a>

`Category`  <a name="cfn-codepipeline-pipeline-stages-actions-actiontypeid-category"></a>
A category defines what kind of action can be taken in the stage, and constrains the provider type for the action\. Valid categories are limited to one of the values below\.  
+ `Source`
+ `Build`
+ `Test`
+ `Deploy`
+ `Invoke`
+ `Approval`
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Owner`  <a name="cfn-codepipeline-pipeline-stages-actions-actiontypeid-owner"></a>
The creator of the action being called\. There are three valid values for the `Owner` field in the action category section within your pipeline structure: `AWS`, `ThirdParty`, and `Custom`\. For more information, see [Valid Action Types and Providers in CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#actions-valid-providers)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Provider`  <a name="cfn-codepipeline-pipeline-stages-actions-actiontypeid-provider"></a>
The provider of the service being called by the action\. Valid providers are determined by the action category\. For example, an action in the Deploy category type might have a provider of AWS CodeDeploy, which would be specified as CodeDeploy\. For more information, see [Valid Action Types and Providers in CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#actions-valid-providers)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-codepipeline-pipeline-stages-actions-actiontypeid-version"></a>
A string that describes the action version\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
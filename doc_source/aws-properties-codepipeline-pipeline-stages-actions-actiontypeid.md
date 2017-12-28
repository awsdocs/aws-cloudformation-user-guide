# AWS CodePipeline Pipeline Stages Actions ActionTypeId<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid"></a>

`ActionTypeId` is a property of the [AWS CodePipeline Pipeline Stages Actions](aws-properties-codepipeline-pipeline-stages-actions.md) property that specifies the action type and provider for an AWS CodePipeline action\.

## Syntax<a name="w3ab2c21c14d394b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-category)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-owner)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-provider)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-version)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-actiontypeid-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-category): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-owner): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-provider): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid-version): String
```

## Properties<a name="w3ab2c21c14d394b7"></a>

`Category`  
A category that defines which action type the owner \(the entity that performs the action\) performs\. The category that you select determine the providers that you can specify for the `Provider` property\. For valid values, see [ActionTypeId](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ActionTypeId.html) in the *AWS CodePipeline API Reference*\.  
*Required: *Yes  
*Type*: String

`Owner`  
The entity that performs the action\. For valid values, see [ActionTypeId](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ActionTypeId.html) in the *AWS CodePipeline API Reference*\.  
*Required: *Yes  
*Type*: String

`Provider`  
The service provider that the action calls\. The providers that you can specify are determined by the category that you select\. For example, a valid provider for the `Deploy` category is AWS CodeDeploy, which you would specify as `CodeDeploy`\.  
*Required: *Yes  
*Type*: String

`Version`  
A version identifier for this action\.  
*Required: *Yes  
*Type*: String
# AWS::CodeBuild::Project ProjectBuildBatchConfig<a name="aws-properties-codebuild-project-projectbuildbatchconfig"></a>

Contains configuration information about a batch build project\.

## Syntax<a name="aws-properties-codebuild-project-projectbuildbatchconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projectbuildbatchconfig-syntax.json"></a>

```
{
  "[CombineArtifacts](#cfn-codebuild-project-projectbuildbatchconfig-combineartifacts)" : Boolean,
  "[Restrictions](#cfn-codebuild-project-projectbuildbatchconfig-restrictions)" : BatchRestrictions,
  "[ServiceRole](#cfn-codebuild-project-projectbuildbatchconfig-servicerole)" : String,
  "[TimeoutInMins](#cfn-codebuild-project-projectbuildbatchconfig-timeoutinmins)" : Integer
}
```

### YAML<a name="aws-properties-codebuild-project-projectbuildbatchconfig-syntax.yaml"></a>

```
  [CombineArtifacts](#cfn-codebuild-project-projectbuildbatchconfig-combineartifacts): Boolean
  [Restrictions](#cfn-codebuild-project-projectbuildbatchconfig-restrictions): 
    BatchRestrictions
  [ServiceRole](#cfn-codebuild-project-projectbuildbatchconfig-servicerole): String
  [TimeoutInMins](#cfn-codebuild-project-projectbuildbatchconfig-timeoutinmins): Integer
```

## Properties<a name="aws-properties-codebuild-project-projectbuildbatchconfig-properties"></a>

`CombineArtifacts`  <a name="cfn-codebuild-project-projectbuildbatchconfig-combineartifacts"></a>
Specifies if the build artifacts for the batch build should be combined into a single artifact location\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Restrictions`  <a name="cfn-codebuild-project-projectbuildbatchconfig-restrictions"></a>
A `BatchRestrictions` object that specifies the restrictions for the batch build\.  
*Required*: No  
*Type*: [BatchRestrictions](aws-properties-codebuild-project-batchrestrictions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRole`  <a name="cfn-codebuild-project-projectbuildbatchconfig-servicerole"></a>
Specifies the service role ARN for the batch build project\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInMins`  <a name="cfn-codebuild-project-projectbuildbatchconfig-timeoutinmins"></a>
Specifies the maximum amount of time, in minutes, that the batch build must be completed in\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
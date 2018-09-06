# AWS CodeBuild Project ProjectTriggers<a name="aws-properties-codebuild-project-projecttriggers"></a>

`ProjectTriggers` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies the environment for an AWS CodeBuild project\.

## Syntax<a name="aws-properties-codebuild-project-projecttriggers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projecttriggers-syntax.json"></a>

```
{
  "[Webhook](#cfn-codebuild-project-projecttriggers-webhook)" : Boolean
}
```

### YAML<a name="aws-properties-codebuild-project-projecttriggers-syntax.yaml"></a>

```
[Webhook](#cfn-codebuild-project-projecttriggers-webhook): Boolean
```

## Properties<a name="w3ab2c21c14d375b7"></a>

`Webhook`  <a name="cfn-codebuild-project-projecttriggers-webhook"></a>
Specifies whether or not to begin automatically rebuilding the source code every time a code change is pushed to the repository\.  
*Required*: No  
*Type*: Boolean
# AWS CodeBuild Project ProjectTriggers<a name="aws-properties-codebuild-project-projecttriggers"></a>

 `ProjectTriggers` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies the environment for an AWS CodeBuild project\. 

## Syntax<a name="aws-properties-codebuild-project-projecttriggers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projecttriggers-syntax.json"></a>

```
{
  "[Webhook](#cfn-codebuild-project-projecttriggers-webhook)" : Boolean
  "[FilterGroups](#cfn-codebuild-project-projecttriggers-filtergroups)" : [[*\[WebhookFilter, \.\.\.\], \.\.\.*](aws-properties-codebuild-project-webhookfilter.md)]
}
```

### YAML<a name="aws-properties-codebuild-project-projecttriggers-syntax.yaml"></a>

```
[Webhook](#cfn-codebuild-project-projecttriggers-webhook): Boolean
[FilterGroups](#cfn-codebuild-project-projecttriggers-filtergroups): 
  - -[* WebhookFilter*](aws-properties-codebuild-project-webhookfilter.md)
```

## Properties<a name="w13ab1c21c10c72c13c33b7"></a>

`Webhook`  <a name="cfn-codebuild-project-projecttriggers-webhook"></a>
Specifies whether or not to begin automatically rebuilding the source code every time a code change is pushed to the repository\.  
*Required*: No  
*Type*: Boolean

`FilterGroups`  <a name="cfn-codebuild-project-projecttriggers-filtergroups"></a>
A list of lists of `WebhookFilter` objects used to determine which webhook events are triggered\. At least one `WebhookFilter` in the array must specify `EVENT` as its type\.  
*Required*: No  
*Type*: A list of a list of [AWS CodeBuild Project WebhookFilter](aws-properties-codebuild-project-webhookfilter.md) objects\.
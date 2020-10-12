# AWS::CodeBuild::Project ProjectTriggers<a name="aws-properties-codebuild-project-projecttriggers"></a>

 `ProjectTriggers` is a property of the [AWS CodeBuild Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html) resource that specifies webhooks that trigger an AWS CodeBuild build\. 

## Syntax<a name="aws-properties-codebuild-project-projecttriggers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projecttriggers-syntax.json"></a>

```
{
  "[FilterGroups](#cfn-codebuild-project-projecttriggers-filtergroups)" : [ FilterGroup, ... ],
  "[Webhook](#cfn-codebuild-project-projecttriggers-webhook)" : Boolean
}
```

### YAML<a name="aws-properties-codebuild-project-projecttriggers-syntax.yaml"></a>

```
  [FilterGroups](#cfn-codebuild-project-projecttriggers-filtergroups): 
    - FilterGroup
  [Webhook](#cfn-codebuild-project-projecttriggers-webhook): Boolean
```

## Properties<a name="aws-properties-codebuild-project-projecttriggers-properties"></a>

`FilterGroups`  <a name="cfn-codebuild-project-projecttriggers-filtergroups"></a>
 A list of lists of `WebhookFilter` objects used to determine which webhook events are triggered\. At least one `WebhookFilter` in the array must specify `EVENT` as its type\.   
*Required*: No  
*Type*: List of [FilterGroup](aws-properties-codebuild-project-filtergroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Webhook`  <a name="cfn-codebuild-project-projecttriggers-webhook"></a>
 Specifies whether or not to begin automatically rebuilding the source code every time a code change is pushed to the repository\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
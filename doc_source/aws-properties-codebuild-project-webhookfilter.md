# AWS::CodeBuild::Project WebhookFilter<a name="aws-properties-codebuild-project-webhookfilter"></a>

`WebhookFilter` is a structure of the `FilterGroups` property on the [AWS CodeBuild Project ProjectTriggers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projecttriggers.html) property type that specifies which webhooks trigger an AWS CodeBuild build\.

## Syntax<a name="aws-properties-codebuild-project-webhookfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-webhookfilter-syntax.json"></a>

```
{
  "[ExcludeMatchedPattern](#cfn-codebuild-project-webhookfilter-excludematchedpattern)" : Boolean,
  "[Pattern](#cfn-codebuild-project-webhookfilter-pattern)" : String,
  "[Type](#cfn-codebuild-project-webhookfilter-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-webhookfilter-syntax.yaml"></a>

```
  [ExcludeMatchedPattern](#cfn-codebuild-project-webhookfilter-excludematchedpattern): Boolean
  [Pattern](#cfn-codebuild-project-webhookfilter-pattern): String
  [Type](#cfn-codebuild-project-webhookfilter-type): String
```

## Properties<a name="aws-properties-codebuild-project-webhookfilter-properties"></a>

`ExcludeMatchedPattern`  <a name="cfn-codebuild-project-webhookfilter-excludematchedpattern"></a>
 Used to indicate that the `pattern` determines which webhook events do not trigger a build\. If true, then a webhook event that does not match the `pattern` triggers a build\. If false, then a webhook event that matches the `pattern` triggers a build\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pattern`  <a name="cfn-codebuild-project-webhookfilter-pattern"></a>
 For a `WebHookFilter` that uses `EVENT` type, a comma\-separated string that specifies one or more events\. For example, the webhook filter `PUSH, PULL_REQUEST_CREATED, PULL_REQUEST_UPDATED` allows all push, pull request created, and pull request updated events to trigger a build\.   
 For a `WebHookFilter` that uses any of the other filter types, a regular expression pattern\. For example, a `WebHookFilter` that uses `HEAD_REF` for its `type` and the pattern `^refs/heads/` triggers a build when the head reference is a branch with a reference name `refs/heads/branch-name`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-webhookfilter-type"></a>
 The type of webhook filter\. There are six webhook filter types: `EVENT`, `ACTOR_ACCOUNT_ID`, `HEAD_REF`, `BASE_REF`, `FILE_PATH`, and `COMMIT_MESSAGE`\.     
 EVENT   
 A webhook event triggers a build when the provided `pattern` matches one of five event types: `PUSH`, `PULL_REQUEST_CREATED`, `PULL_REQUEST_UPDATED`, `PULL_REQUEST_REOPENED`, and `PULL_REQUEST_MERGED`\. The `EVENT` patterns are specified as a comma\-separated string\. For example, `PUSH, PULL_REQUEST_CREATED, PULL_REQUEST_UPDATED` filters all push, pull request created, and pull request updated events\.   
 The `PULL_REQUEST_REOPENED` works with GitHub and GitHub Enterprise only\.   
 ACTOR\_ACCOUNT\_ID   
 A webhook event triggers a build when a GitHub, GitHub Enterprise, or Bitbucket account ID matches the regular expression `pattern`\.   
 HEAD\_REF   
 A webhook event triggers a build when the head reference matches the regular expression `pattern`\. For example, `refs/heads/branch-name` and `refs/tags/tag-name`\.   
 Works with GitHub and GitHub Enterprise push, GitHub and GitHub Enterprise pull request, Bitbucket push, and Bitbucket pull request events\.   
 BASE\_REF   
 A webhook event triggers a build when the base reference matches the regular expression `pattern`\. For example, `refs/heads/branch-name`\.   
 Works with pull request events only\.   
 FILE\_PATH   
 A webhook triggers a build when the path of a changed file matches the regular expression `pattern`\.   
 Works with GitHub and Bitbucket events push and pull requests events\. Also works with GitHub Enterprise push events, but does not work with GitHub Enterprise pull request events\.   
COMMIT\_MESSAGE  
A webhook triggers a build when the head commit message matches the regular expression `pattern`\.  
 Works with GitHub and Bitbucket events push and pull requests events\. Also works with GitHub Enterprise push events, but does not work with GitHub Enterprise pull request events\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `ACTOR_ACCOUNT_ID | BASE_REF | COMMIT_MESSAGE | EVENT | FILE_PATH | HEAD_REF`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::CodeBuild::Project BuildStatusConfig<a name="aws-properties-codebuild-project-buildstatusconfig"></a>

Contains information that defines how the AWS CodeBuild build project reports the build status to the source provider\. 

## Syntax<a name="aws-properties-codebuild-project-buildstatusconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-buildstatusconfig-syntax.json"></a>

```
{
  "[Context](#cfn-codebuild-project-buildstatusconfig-context)" : String,
  "[TargetUrl](#cfn-codebuild-project-buildstatusconfig-targeturl)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-buildstatusconfig-syntax.yaml"></a>

```
  [Context](#cfn-codebuild-project-buildstatusconfig-context): String
  [TargetUrl](#cfn-codebuild-project-buildstatusconfig-targeturl): String
```

## Properties<a name="aws-properties-codebuild-project-buildstatusconfig-properties"></a>

`Context`  <a name="cfn-codebuild-project-buildstatusconfig-context"></a>
Specifies the context of the build status CodeBuild sends to the source provider\. The usage of this parameter depends on the source provider\.    
Bitbucket  
This parameter is used for the `name` parameter in the Bitbucket commit status\. For more information, see [build](https://developer.atlassian.com/bitbucket/api/2/reference/resource/repositories/%7Bworkspace%7D/%7Brepo_slug%7D/commit/%7Bnode%7D/statuses/build) in the Bitbucket API documentation\.  
GitHub/GitHub Enterprise Server  
This parameter is used for the `context` parameter in the GitHub commit status\. For more information, see [Create a commit status](https://developer.github.com/v3/repos/statuses/#create-a-commit-status) in the GitHub developer guide\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetUrl`  <a name="cfn-codebuild-project-buildstatusconfig-targeturl"></a>
Specifies the target url of the build status CodeBuild sends to the source provider\. The usage of this parameter depends on the source provider\.    
Bitbucket  
This parameter is used for the `url` parameter in the Bitbucket commit status\. For more information, see [build](https://developer.atlassian.com/bitbucket/api/2/reference/resource/repositories/%7Bworkspace%7D/%7Brepo_slug%7D/commit/%7Bnode%7D/statuses/build) in the Bitbucket API documentation\.  
GitHub/GitHub Enterprise Server  
This parameter is used for the `target_url` parameter in the GitHub commit status\. For more information, see [Create a commit status](https://developer.github.com/v3/repos/statuses/#create-a-commit-status) in the GitHub developer guide\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS CodeDeploy DeploymentGroup Deployment Revision GitHubLocation<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation"></a>

`GitHubLocation` is a property of the [AWS CodeDeploy DeploymentGroup Deployment Revision](aws-properties-codedeploy-deploymentgroup-deployment-revision.md) property that specifies the location of an application revision that is stored in GitHub\.

## Syntax<a name="w3ab2c21c14d341b5"></a>

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-commitid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-repository)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-commitid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-repository): String
```

## Properties<a name="w3ab2c21c14d341b7"></a>

`CommitId`  
The SHA1 commit ID of the GitHub commit to use as your application revision\.  
*Required: *Yes  
*Type*: String

`Repository`  
The GitHub account and repository name that includes the application revision\. Specify the value as `account/repository_name`\.  
*Required: *Yes  
*Type*: String
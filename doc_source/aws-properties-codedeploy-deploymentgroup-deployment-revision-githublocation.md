# AWS CodeDeploy DeploymentGroup Deployment Revision GitHubLocation<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation"></a>

`GitHubLocation` is a property of the [AWS CodeDeploy DeploymentGroup Revision](aws-properties-codedeploy-deploymentgroup-deployment-revision.md) property that specifies the location of an application revision that is stored in GitHub\.

## Syntax<a name="w4ab1c21c10c72c21c47b5"></a>

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-syntax.json"></a>

```
{
  "[CommitId](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-commitid)" : String,
  "[Repository](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-repository)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-syntax.yaml"></a>

```
[CommitId](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-commitid): String
[Repository](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-repository): String
```

## Properties<a name="w4ab1c21c10c72c21c47b7"></a>

`CommitId`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-commitid"></a>
The SHA1 commit ID of the GitHub commit to use as your application revision\.  
*Required*: Yes  
*Type*: String

`Repository`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-repository"></a>
The GitHub account and repository name that includes the application revision\. Specify the value as `account/repository_name`\.  
*Required*: Yes  
*Type*: String
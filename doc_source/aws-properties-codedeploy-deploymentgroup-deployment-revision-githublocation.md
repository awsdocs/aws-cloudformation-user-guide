# AWS::CodeDeploy::DeploymentGroup GitHubLocation<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation"></a>

 `GitHubLocation` is a property of the [CodeDeploy DeploymentGroup Revision](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codedeploy-deploymentgroup-deployment-revision.html) property that specifies the location of an application revision that is stored in GitHub\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-properties"></a>

`CommitId`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-commitid"></a>
The SHA1 commit ID of the GitHub commit that represents the bundled artifacts for the application revision\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Repository`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation-repository"></a>
The GitHub account and repository pair that stores a reference to the commit that represents the bundled artifacts for the application revision\.   
Specify the value as `account/repository`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
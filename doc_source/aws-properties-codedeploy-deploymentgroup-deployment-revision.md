# CodeDeploy DeploymentGroup Revision<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision"></a>

`Revision` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) property that defines the location of the CodeDeploy application revision to deploy\.

## Syntax<a name="w13ab1c21c10c78c21c61b5"></a>

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-syntax.json"></a>

```
{
  "[GitHubLocation](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation)" : GitHubLocation,
  "[RevisionType](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-revisiontype)" : String,
  "[S3Location](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location)" : S3Location
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-syntax.yaml"></a>

```
[GitHubLocation](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation):
  GitHubLocation
[RevisionType](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-revisiontype): String
[S3Location](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location):
  S3Location
```

## Properties<a name="w13ab1c21c10c78c21c61b7"></a>

`GitHubLocation`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation"></a>
If your application revision is stored in GitHub, information about the location where it is stored\.  
*Required*: No  
*Type*: [CodeDeploy DeploymentGroup Deployment Revision GitHubLocation](aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation.md)

`RevisionType`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-revisiontype"></a>
The application revision's location, such as in an S3 bucket or GitHub repository\. For valid values, see [RevisionLocation](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_RevisionLocation.html) in the *AWS CodeDeploy API Reference*\.  
*Required*: No  
*Type*: String

`S3Location`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location"></a>
If the application revision is stored in an S3 bucket, information about the location\.  
*Required*: No  
*Type*: [CodeDeploy DeploymentGroup Deployment Revision S3Location](aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location.md)
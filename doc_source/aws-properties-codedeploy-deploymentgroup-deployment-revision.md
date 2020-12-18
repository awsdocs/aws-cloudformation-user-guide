# AWS::CodeDeploy::DeploymentGroup RevisionLocation<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision"></a>

 `RevisionLocation` is a property that defines the location of the CodeDeploy application revision to deploy\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-properties"></a>

`GitHubLocation`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-githublocation"></a>
Information about the location of application artifacts stored in GitHub\.  
*Required*: No  
*Type*: [GitHubLocation](aws-properties-codedeploy-deploymentgroup-deployment-revision-githublocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RevisionType`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-revisiontype"></a>
The type of application revision:  
+ S3: An application revision stored in Amazon S3\.
+ GitHub: An application revision stored in GitHub \(EC2/On\-premises deployments only\)\.
+ String: A YAML\-formatted or JSON\-formatted string \(AWS Lambda deployments only\)\.
+ AppSpecContent: An `AppSpecContent` object that contains the contents of an AppSpec file for an AWS Lambda or Amazon ECS deployment\. The content is formatted as JSON or YAML stored as a RawString\.
*Required*: No  
*Type*: String  
*Allowed values*: `AppSpecContent | GitHub | S3 | String`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Location`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location"></a>
Information about the location of a revision stored in Amazon S3\.   
*Required*: No  
*Type*: [S3Location](aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
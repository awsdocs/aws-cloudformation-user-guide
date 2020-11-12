# AWS::CodeDeploy::DeploymentGroup S3Location<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location"></a>

 `S3Location` is a property of the [ CodeDeploy DeploymentGroup Revision ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codedeploy-deploymentgroup-deployment-revision.html) property that specifies the location of an application revision that is stored in Amazon Simple Storage Service \(S3\)\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location-syntax.json"></a>

```
{
  "[Bucket](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bucket)" : String,
  "[BundleType](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bundletype)" : String,
  "[ETag](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-etag)" : String,
  "[Key](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-key)" : String,
  "[Version](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-value)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location-syntax.yaml"></a>

```
  [Bucket](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bucket): String
  [BundleType](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bundletype): String
  [ETag](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-etag): String
  [Key](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-key): String
  [Version](#cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-value): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location-properties"></a>

`Bucket`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bucket"></a>
The name of the Amazon S3 bucket where the application revision is stored\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BundleType`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bundletype"></a>
The file type of the application revision\. Must be one of the following:  
+ JSON
+ tar: A tar archive file\.
+ tgz: A compressed tar archive file\.
+ YAML
+ zip: A zip archive file\.
*Required*: No  
*Type*: String  
*Allowed values*: `JSON | tar | tgz | YAML | zip`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ETag`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-etag"></a>
The ETag of the Amazon S3 object that represents the bundled artifacts for the application revision\.  
If the ETag is not specified as an input parameter, ETag validation of the object is skipped\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-key"></a>
The name of the Amazon S3 object that represents the bundled artifacts for the application revision\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-value"></a>
A specific version of the Amazon S3 object that represents the bundled artifacts for the application revision\.  
If the version is not specified, the system uses the most recent version by default\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
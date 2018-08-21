# AWS CodeDeploy DeploymentGroup Deployment Revision S3Location<a name="aws-properties-codedeploy-deploymentgroup-deployment-revision-s3location"></a>

`S3Location` is a property of the [AWS CodeDeploy DeploymentGroup Deployment Revision](aws-properties-codedeploy-deploymentgroup-deployment-revision.md) property that specifies the location of an application revision that is stored in Amazon Simple Storage Service \(Amazon S3\)\.

## Syntax<a name="w3ab2c21c14d419b5"></a>

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

## Properties<a name="w3ab2c21c14d419b7"></a>

`Bucket`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bucket"></a>
The name of the S3 bucket where the application revision is stored\.  
*Required*: Yes  
*Type*: String

`BundleType`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-bundletype"></a>
The file type of the application revision, such as `tar`, `tgz`, or `zip`\. For valid values, see [S3Location](http://docs.aws.amazon.com/codedeploy/latest/APIReference/API_S3Location.html) in the *AWS CodeDeploy API Reference*\.  
*Required*: Yes  
*Type*: String

`ETag`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-etag"></a>
The Amazon S3 ETag \(a file checksum\) of the application revision\. If you don't specify a value, AWS CodeDeploy skips the ETag validation of your application revision\.  
*Required*: No  
*Type*: String

`Key`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-key"></a>
The file name of the application revision \(Amazon S3 object name\)\.  
*Required*: Yes  
*Type*: String

`Version`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision-s3location-value"></a>
For versioning\-enabled buckets, a specific version of the application revision\.  
*Required*: No  
*Type*: String
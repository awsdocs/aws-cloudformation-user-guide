# AWS::Synthetics::Canary ArtifactConfig<a name="aws-properties-synthetics-canary-artifactconfig"></a>

A structure that contains the configuration for canary artifacts, including the encryption\-at\-rest settings for artifacts that the canary uploads to Amazon S3\. 

## Syntax<a name="aws-properties-synthetics-canary-artifactconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-artifactconfig-syntax.json"></a>

```
{
  "[S3Encryption](#cfn-synthetics-canary-artifactconfig-s3encryption)" : S3Encryption
}
```

### YAML<a name="aws-properties-synthetics-canary-artifactconfig-syntax.yaml"></a>

```
  [S3Encryption](#cfn-synthetics-canary-artifactconfig-s3encryption): 
    S3Encryption
```

## Properties<a name="aws-properties-synthetics-canary-artifactconfig-properties"></a>

`S3Encryption`  <a name="cfn-synthetics-canary-artifactconfig-s3encryption"></a>
A structure that contains the configuration of the encryption\-at\-rest settings for artifacts that the canary uploads to Amazon S3\. Artifact encryption functionality is available only for canaries that use Synthetics runtime version syn\-nodejs\-puppeteer\-3\.3 or later\. For more information, see [Encrypting canary artifacts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_artifact_encryption.html)\.  
*Required*: No  
*Type*: [S3Encryption](aws-properties-synthetics-canary-s3encryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
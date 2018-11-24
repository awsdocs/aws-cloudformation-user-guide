# AWS CodePipeline Pipeline ArtifactStore<a name="aws-properties-codepipeline-pipeline-artifactstore"></a>

`ArtifactStore` is a property of the [AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md) resource that defines the S3 location where AWS CodePipeline stores pipeline artifacts\.

## Syntax<a name="w4ab1c21c14d498b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-artifactstore-syntax.json"></a>

```
{
  "[EncryptionKey](#cfn-codepipeline-pipeline-artifactstore-encryptionkey)" : EncryptionKey,
  "[Location](#cfn-codepipeline-pipeline-artifactstore-location)" : String,
  "[Type](#cfn-codepipeline-pipeline-artifactstore-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-artifactstore-syntax.yaml"></a>

```
[EncryptionKey](#cfn-codepipeline-pipeline-artifactstore-encryptionkey): EncryptionKey
[Location](#cfn-codepipeline-pipeline-artifactstore-location): String
[Type](#cfn-codepipeline-pipeline-artifactstore-type): String
```

## Properties<a name="w4ab1c21c14d498b7"></a>

`EncryptionKey`  <a name="cfn-codepipeline-pipeline-artifactstore-encryptionkey"></a>
The encryption key AWS CodePipeline uses to encrypt the data in the artifact store, such as an AWS Key Management Service \(AWS KMS\) key\. If you don't specify a key, AWS CodePipeline uses the default key for Amazon Simple Storage Service \(Amazon S3\)\.  
*Required*: No  
*Type*: [AWS CodePipeline Pipeline ArtifactStore EncryptionKey](aws-properties-codepipeline-pipeline-artifactstore-encryptionkey.md)

`Location`  <a name="cfn-codepipeline-pipeline-artifactstore-location"></a>
The name of the S3 bucket where AWS CodePipeline stores artifacts for a pipeline\.  
*Required*: Yes  
*Type*: String

`Type`  <a name="cfn-codepipeline-pipeline-artifactstore-type"></a>
The type of the artifact store, such as Amazon S3\. For valid values, see [ArtifactStore](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ArtifactStore.html) in the *AWS CodePipeline API Reference*\.  
*Required*: Yes  
*Type*: String
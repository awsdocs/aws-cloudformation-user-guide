# AWS CodePipeline Pipeline ArtifactStore EncryptionKey<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey"></a>

`EncryptionKey` is a property of the [AWS CodePipeline Pipeline ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md) property that specifies which key AWS CodePipeline uses to encrypt data in the artifact store, such as an AWS Key Management Service \(AWS KMS\) key\.

## Syntax<a name="w3ab2c21c14d378b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-type): String
```

## Properties<a name="w3ab2c21c14d378b7"></a>

`Id`  
The ID of the key\. For an AWS KMS key, specify the key ID or key Amazon Resource Number \(ARN\)\.  
*Required: *Yes  
*Type*: String

`Type`  
The type of encryption key, such as `KMS`\. For valid values, see [EncryptionKey](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_EncryptionKey.html) in the *AWS CodePipeline API Reference*\.  
*Required: *Yes  
*Type*: String
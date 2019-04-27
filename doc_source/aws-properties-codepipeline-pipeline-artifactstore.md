# AWS::CodePipeline::Pipeline ArtifactStore<a name="aws-properties-codepipeline-pipeline-artifactstore"></a>

The Amazon S3 bucket where artifacts are stored for the pipeline\.

## Syntax<a name="aws-properties-codepipeline-pipeline-artifactstore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-artifactstore-syntax.json"></a>

```
{
  "[EncryptionKey](#cfn-codepipeline-pipeline-artifactstore-encryptionkey)" : [EncryptionKey](aws-properties-codepipeline-pipeline-artifactstore-encryptionkey.md),
  "[Location](#cfn-codepipeline-pipeline-artifactstore-location)" : String,
  "[Type](#cfn-codepipeline-pipeline-artifactstore-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-artifactstore-syntax.yaml"></a>

```
﻿  [EncryptionKey](#cfn-codepipeline-pipeline-artifactstore-encryptionkey) : [EncryptionKey](aws-properties-codepipeline-pipeline-artifactstore-encryptionkey.md)
﻿  [Location](#cfn-codepipeline-pipeline-artifactstore-location) : String
﻿  [Type](#cfn-codepipeline-pipeline-artifactstore-type) : String
```

## Properties<a name="aws-properties-codepipeline-pipeline-artifactstore-properties"></a>

`EncryptionKey`  <a name="cfn-codepipeline-pipeline-artifactstore-encryptionkey"></a>
The encryption key used to encrypt the data in the artifact store, such as an AWS Key Management Service \(AWS KMS\) key\. If this is undefined, the default key for Amazon S3 is used\.  
*Required*: No  
*Type*: [EncryptionKey](aws-properties-codepipeline-pipeline-artifactstore-encryptionkey.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-codepipeline-pipeline-artifactstore-location"></a>
The Amazon S3 bucket used for storing the artifacts for a pipeline\. You can specify the name of an S3 bucket but not a folder within the bucket\. A folder to contain the pipeline artifacts is created for you based on the name of the pipeline\. You can use any Amazon S3 bucket in the same AWS Region as the pipeline to store your pipeline artifacts\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-zA-Z0-9\-\.]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codepipeline-pipeline-artifactstore-type"></a>
The type of the artifact store, such as S3\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
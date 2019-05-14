# AWS::CodePipeline::Pipeline EncryptionKey<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey"></a>

Represents information about the key used to encrypt data in the artifact store, such as an AWS Key Management Service \(AWS KMS\) key\.

## Syntax<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-syntax.json"></a>

```
{
  "[Id](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-id)" : String,
  "[Type](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-syntax.yaml"></a>

```
﻿  [Id](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-id) : String
﻿  [Type](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-type) : String
```

## Properties<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-properties"></a>

`Id`  <a name="cfn-codepipeline-pipeline-artifactstore-encryptionkey-id"></a>
The ID used to identify the key\. For an AWS KMS key, this is the key ID or key ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codepipeline-pipeline-artifactstore-encryptionkey-type"></a>
The type of encryption key, such as an AWS Key Management Service \(AWS KMS\) key\. When creating or updating a pipeline, the value must be set to 'KMS'\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
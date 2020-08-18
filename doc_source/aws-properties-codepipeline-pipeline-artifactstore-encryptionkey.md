# AWS::CodePipeline::Pipeline EncryptionKey<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey"></a>

Represents information about the key used to encrypt data in the artifact store, such as an AWS Key Management Service \(AWS KMS\) key\.

`EncryptionKey` is a property of the [ArtifactStore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codepipeline-pipeline-artifactstore.html) property type\.

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
  [Id](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-id): String
  [Type](#cfn-codepipeline-pipeline-artifactstore-encryptionkey-type): String
```

## Properties<a name="aws-properties-codepipeline-pipeline-artifactstore-encryptionkey-properties"></a>

`Id`  <a name="cfn-codepipeline-pipeline-artifactstore-encryptionkey-id"></a>
The ID used to identify the key\. For an AWS KMS key, you can use the key ID, the key ARN, or the alias ARN\.  
Aliases are recognized only in the account that created the customer master key \(CMK\)\. For cross\-account actions, you can only use the key ID or key ARN to identify the key\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codepipeline-pipeline-artifactstore-encryptionkey-type"></a>
The type of encryption key, such as an AWS Key Management Service \(AWS KMS\) key\. When creating or updating a pipeline, the value must be set to 'KMS'\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
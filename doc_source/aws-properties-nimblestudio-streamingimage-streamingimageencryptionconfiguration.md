# AWS::NimbleStudio::StreamingImage StreamingImageEncryptionConfiguration<a name="aws-properties-nimblestudio-streamingimage-streamingimageencryptionconfiguration"></a>

Specifies how a streaming image is encrypted\.

## Syntax<a name="aws-properties-nimblestudio-streamingimage-streamingimageencryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-streamingimage-streamingimageencryptionconfiguration-syntax.json"></a>

```
{
  "[KeyArn](#cfn-nimblestudio-streamingimage-streamingimageencryptionconfiguration-keyarn)" : String,
  "[KeyType](#cfn-nimblestudio-streamingimage-streamingimageencryptionconfiguration-keytype)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-streamingimage-streamingimageencryptionconfiguration-syntax.yaml"></a>

```
  [KeyArn](#cfn-nimblestudio-streamingimage-streamingimageencryptionconfiguration-keyarn): String
  [KeyType](#cfn-nimblestudio-streamingimage-streamingimageencryptionconfiguration-keytype): String
```

## Properties<a name="aws-properties-nimblestudio-streamingimage-streamingimageencryptionconfiguration-properties"></a>

`KeyArn`  <a name="cfn-nimblestudio-streamingimage-streamingimageencryptionconfiguration-keyarn"></a>
The ARN for a KMS key that is used to encrypt studio data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyType`  <a name="cfn-nimblestudio-streamingimage-streamingimageencryptionconfiguration-keytype"></a>
The type of KMS key that is used to encrypt studio data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
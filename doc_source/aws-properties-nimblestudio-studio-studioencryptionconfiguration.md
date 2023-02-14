# AWS::NimbleStudio::Studio StudioEncryptionConfiguration<a name="aws-properties-nimblestudio-studio-studioencryptionconfiguration"></a>

Configuration of the encryption method that is used for the studio\.

## Syntax<a name="aws-properties-nimblestudio-studio-studioencryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studio-studioencryptionconfiguration-syntax.json"></a>

```
{
  "[KeyArn](#cfn-nimblestudio-studio-studioencryptionconfiguration-keyarn)" : String,
  "[KeyType](#cfn-nimblestudio-studio-studioencryptionconfiguration-keytype)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studio-studioencryptionconfiguration-syntax.yaml"></a>

```
  [KeyArn](#cfn-nimblestudio-studio-studioencryptionconfiguration-keyarn): String
  [KeyType](#cfn-nimblestudio-studio-studioencryptionconfiguration-keytype): String
```

## Properties<a name="aws-properties-nimblestudio-studio-studioencryptionconfiguration-properties"></a>

`KeyArn`  <a name="cfn-nimblestudio-studio-studioencryptionconfiguration-keyarn"></a>
The ARN for a KMS key that is used to encrypt studio data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyType`  <a name="cfn-nimblestudio-studio-studioencryptionconfiguration-keytype"></a>
The type of KMS key that is used to encrypt studio data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
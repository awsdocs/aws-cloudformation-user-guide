# AWS::MediaPackageV2::OriginEndpoint EncryptionMethod<a name="aws-properties-mediapackagev2-originendpoint-encryptionmethod"></a>

The encryption method associated with the origin endpoint\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-encryptionmethod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-encryptionmethod-syntax.json"></a>

```
{
  "[CmafEncryptionMethod](#cfn-mediapackagev2-originendpoint-encryptionmethod-cmafencryptionmethod)" : String,
  "[TsEncryptionMethod](#cfn-mediapackagev2-originendpoint-encryptionmethod-tsencryptionmethod)" : String
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-encryptionmethod-syntax.yaml"></a>

```
  [CmafEncryptionMethod](#cfn-mediapackagev2-originendpoint-encryptionmethod-cmafencryptionmethod): String
  [TsEncryptionMethod](#cfn-mediapackagev2-originendpoint-encryptionmethod-tsencryptionmethod): String
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-encryptionmethod-properties"></a>

`CmafEncryptionMethod`  <a name="cfn-mediapackagev2-originendpoint-encryptionmethod-cmafencryptionmethod"></a>
The encryption method to use\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CBCS | CENC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TsEncryptionMethod`  <a name="cfn-mediapackagev2-originendpoint-encryptionmethod-tsencryptionmethod"></a>
The encryption method to use\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AES_128 | SAMPLE_AES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
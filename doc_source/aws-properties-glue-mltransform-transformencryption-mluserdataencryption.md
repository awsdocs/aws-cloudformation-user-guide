# AWS::Glue::MLTransform MLUserDataEncryption<a name="aws-properties-glue-mltransform-transformencryption-mluserdataencryption"></a>

The encryption\-at\-rest settings of the transform that apply to accessing user data\.

## Syntax<a name="aws-properties-glue-mltransform-transformencryption-mluserdataencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-mltransform-transformencryption-mluserdataencryption-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-glue-mltransform-transformencryption-mluserdataencryption-kmskeyid)" : String,
  "[MLUserDataEncryptionMode](#cfn-glue-mltransform-transformencryption-mluserdataencryption-mluserdataencryptionmode)" : String
}
```

### YAML<a name="aws-properties-glue-mltransform-transformencryption-mluserdataencryption-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-glue-mltransform-transformencryption-mluserdataencryption-kmskeyid): String
  [MLUserDataEncryptionMode](#cfn-glue-mltransform-transformencryption-mluserdataencryption-mluserdataencryptionmode): String
```

## Properties<a name="aws-properties-glue-mltransform-transformencryption-mluserdataencryption-properties"></a>

`KmsKeyId`  <a name="cfn-glue-mltransform-transformencryption-mluserdataencryption-kmskeyid"></a>
The ID for the customer\-provided KMS key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MLUserDataEncryptionMode`  <a name="cfn-glue-mltransform-transformencryption-mluserdataencryption-mluserdataencryptionmode"></a>
The encryption mode applied to user data\. Valid values are:  
+ DISABLED: encryption is disabled
+ SSEKMS: use of server\-side encryption with AWS Key Management Service \(SSE\-KMS\) for user data stored in Amazon S3\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
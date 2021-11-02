# AWS::HealthLake::FHIRDatastore KmsEncryptionConfig<a name="aws-properties-healthlake-fhirdatastore-kmsencryptionconfig"></a>

 The customer\-managed\-key\(CMK\) used when creating a Data Store\. If a customer owned key is not specified, an Amazon owned key will be used for encryption\. 

## Syntax<a name="aws-properties-healthlake-fhirdatastore-kmsencryptionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-healthlake-fhirdatastore-kmsencryptionconfig-syntax.json"></a>

```
{
  "[CmkType](#cfn-healthlake-fhirdatastore-kmsencryptionconfig-cmktype)" : String,
  "[KmsKeyId](#cfn-healthlake-fhirdatastore-kmsencryptionconfig-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-healthlake-fhirdatastore-kmsencryptionconfig-syntax.yaml"></a>

```
  [CmkType](#cfn-healthlake-fhirdatastore-kmsencryptionconfig-cmktype): String
  [KmsKeyId](#cfn-healthlake-fhirdatastore-kmsencryptionconfig-kmskeyid): String
```

## Properties<a name="aws-properties-healthlake-fhirdatastore-kmsencryptionconfig-properties"></a>

`CmkType`  <a name="cfn-healthlake-fhirdatastore-kmsencryptionconfig-cmktype"></a>
 The type of customer\-managed\-key\(CMK\) used for encryption\. The two types of supported CMKs are customer owned CMKs and Amazon owned CMKs\. For more information on CMK types, see [KmsEncryptionConfig](https://docs.aws.amazon.com/healthlake/latest/APIReference/API_KmsEncryptionConfig.html#HealthLake-Type-KmsEncryptionConfig-CmkType)\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-healthlake-fhirdatastore-kmsencryptionconfig-kmskeyid"></a>
 The KMS encryption key id/alias used to encrypt the Data Store contents at rest\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `400`  
*Pattern*: `(arn:aws((-us-gov)|(-iso)|(-iso-b)|(-cn))?:kms:)?([a-z]{2}-[a-z]+(-[a-z]+)?-\d:)?(\d{12}:)?(((key/)?[a-zA-Z0-9-_]+)|(alias/[a-zA-Z0-9:/_-]+))`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
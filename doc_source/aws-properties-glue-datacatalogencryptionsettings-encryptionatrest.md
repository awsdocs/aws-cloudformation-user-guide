# AWS::Glue::DataCatalogEncryptionSettings EncryptionAtRest<a name="aws-properties-glue-datacatalogencryptionsettings-encryptionatrest"></a>

Specifies the encryption\-at\-rest configuration for the Data Catalog\.

## Syntax<a name="aws-properties-glue-datacatalogencryptionsettings-encryptionatrest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-datacatalogencryptionsettings-encryptionatrest-syntax.json"></a>

```
{
  "[CatalogEncryptionMode](#cfn-glue-datacatalogencryptionsettings-encryptionatrest-catalogencryptionmode)" : String,
  "[SseAwsKmsKeyId](#cfn-glue-datacatalogencryptionsettings-encryptionatrest-sseawskmskeyid)" : String
}
```

### YAML<a name="aws-properties-glue-datacatalogencryptionsettings-encryptionatrest-syntax.yaml"></a>

```
  [CatalogEncryptionMode](#cfn-glue-datacatalogencryptionsettings-encryptionatrest-catalogencryptionmode): String
  [SseAwsKmsKeyId](#cfn-glue-datacatalogencryptionsettings-encryptionatrest-sseawskmskeyid): String
```

## Properties<a name="aws-properties-glue-datacatalogencryptionsettings-encryptionatrest-properties"></a>

`CatalogEncryptionMode`  <a name="cfn-glue-datacatalogencryptionsettings-encryptionatrest-catalogencryptionmode"></a>
The encryption\-at\-rest mode for encrypting Data Catalog data\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | SSE-KMS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SseAwsKmsKeyId`  <a name="cfn-glue-datacatalogencryptionsettings-encryptionatrest-sseawskmskeyid"></a>
The ID of the AWS KMS key to use for encryption at rest\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Glue::DataCatalogEncryptionSettings ConnectionPasswordEncryption<a name="aws-properties-glue-datacatalogencryptionsettings-connectionpasswordencryption"></a>

The data structure used by the Data Catalog to encrypt the password as part of `CreateConnection` or `UpdateConnection` and store it in the `ENCRYPTED_PASSWORD` field in the connection properties\. You can enable catalog encryption or only password encryption\.

When a `CreationConnection` request arrives containing a password, the Data Catalog first encrypts the password using your AWS KMS key\. It then encrypts the whole connection object again if catalog encryption is also enabled\.

This encryption requires that you set AWS KMS key permissions to enable or restrict access on the password key according to your security requirements\. For example, you might want only administrators to have decrypt permission on the password key\.

## Syntax<a name="aws-properties-glue-datacatalogencryptionsettings-connectionpasswordencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-datacatalogencryptionsettings-connectionpasswordencryption-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-glue-datacatalogencryptionsettings-connectionpasswordencryption-kmskeyid)" : String,
  "[ReturnConnectionPasswordEncrypted](#cfn-glue-datacatalogencryptionsettings-connectionpasswordencryption-returnconnectionpasswordencrypted)" : Boolean
}
```

### YAML<a name="aws-properties-glue-datacatalogencryptionsettings-connectionpasswordencryption-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-glue-datacatalogencryptionsettings-connectionpasswordencryption-kmskeyid): String
  [ReturnConnectionPasswordEncrypted](#cfn-glue-datacatalogencryptionsettings-connectionpasswordencryption-returnconnectionpasswordencrypted): Boolean
```

## Properties<a name="aws-properties-glue-datacatalogencryptionsettings-connectionpasswordencryption-properties"></a>

`KmsKeyId`  <a name="cfn-glue-datacatalogencryptionsettings-connectionpasswordencryption-kmskeyid"></a>
An AWS KMS key that is used to encrypt the connection password\.  
If connection password protection is enabled, the caller of `CreateConnection` and `UpdateConnection` needs at least `kms:Encrypt` permission on the specified AWS KMS key, to encrypt passwords before storing them in the Data Catalog\. You can set the decrypt permission to enable or restrict access on the password key according to your security requirements\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReturnConnectionPasswordEncrypted`  <a name="cfn-glue-datacatalogencryptionsettings-connectionpasswordencryption-returnconnectionpasswordencrypted"></a>
When the `ReturnConnectionPasswordEncrypted` flag is set to "true", passwords remain encrypted in the responses of `GetConnection` and `GetConnections`\. This encryption takes effect independently from catalog encryption\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
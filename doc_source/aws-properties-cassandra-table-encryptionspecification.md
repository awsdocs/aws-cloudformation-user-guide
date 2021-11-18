# AWS::Cassandra::Table EncryptionSpecification<a name="aws-properties-cassandra-table-encryptionspecification"></a>

Specifies the encryption at rest option selected for the table\. 

## Syntax<a name="aws-properties-cassandra-table-encryptionspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cassandra-table-encryptionspecification-syntax.json"></a>

```
{
  "[EncryptionType](#cfn-cassandra-table-encryptionspecification-encryptiontype)" : String,
  "[KmsKeyIdentifier](#cfn-cassandra-table-encryptionspecification-kmskeyidentifier)" : String
}
```

### YAML<a name="aws-properties-cassandra-table-encryptionspecification-syntax.yaml"></a>

```
  [EncryptionType](#cfn-cassandra-table-encryptionspecification-encryptiontype): String
  [KmsKeyIdentifier](#cfn-cassandra-table-encryptionspecification-kmskeyidentifier): String
```

## Properties<a name="aws-properties-cassandra-table-encryptionspecification-properties"></a>

`EncryptionType`  <a name="cfn-cassandra-table-encryptionspecification-encryptiontype"></a>
The encryption at rest options for the table\.  
+ **AWS owned key** \(default\) \- `AWS_OWNED_KMS_KEY`
+ **Customer managed key** \- `CUSTOMER_MANAGED_KMS_KEY`
**Important**  
If you choose `CUSTOMER_MANAGED_KMS_KEY`, a `kms_key_identifier` in the format of a key ARN is required\. 
Valid values: `CUSTOMER_MANAGED_KMS_KEY` \| `AWS_OWNED_KMS_KEY`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyIdentifier`  <a name="cfn-cassandra-table-encryptionspecification-kmskeyidentifier"></a>
Requires a `kms_key_identifier` in the format of a key ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::QLDB::Ledger<a name="aws-resource-qldb-ledger"></a>

The `AWS::QLDB::Ledger` resource specifies a new Amazon Quantum Ledger Database \(Amazon QLDB\) ledger in your AWS account\. Amazon QLDB is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log owned by a central trusted authority\. You can use QLDB to track all application data changes, and maintain a complete and verifiable history of changes over time\.

For more information, see [CreateLedger](https://docs.aws.amazon.com/qldb/latest/developerguide/API_CreateLedger.html) in the *Amazon QLDB API Reference*\.

## Syntax<a name="aws-resource-qldb-ledger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-qldb-ledger-syntax.json"></a>

```
{
  "Type" : "AWS::QLDB::Ledger",
  "Properties" : {
      "[DeletionProtection](#cfn-qldb-ledger-deletionprotection)" : Boolean,
      "[KmsKey](#cfn-qldb-ledger-kmskey)" : String,
      "[Name](#cfn-qldb-ledger-name)" : String,
      "[PermissionsMode](#cfn-qldb-ledger-permissionsmode)" : String,
      "[Tags](#cfn-qldb-ledger-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-qldb-ledger-syntax.yaml"></a>

```
Type: AWS::QLDB::Ledger
Properties: 
  [DeletionProtection](#cfn-qldb-ledger-deletionprotection): Boolean
  [KmsKey](#cfn-qldb-ledger-kmskey): String
  [Name](#cfn-qldb-ledger-name): String
  [PermissionsMode](#cfn-qldb-ledger-permissionsmode): String
  [Tags](#cfn-qldb-ledger-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-qldb-ledger-properties"></a>

`DeletionProtection`  <a name="cfn-qldb-ledger-deletionprotection"></a>
Specifies whether the ledger is protected from being deleted by any user\. If not defined during ledger creation, this feature is enabled \(`true`\) by default\.  
If deletion protection is enabled, you must first disable it before you can delete the ledger\. You can disable it by calling the `UpdateLedger` operation to set this parameter to `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKey`  <a name="cfn-qldb-ledger-kmskey"></a>
The key in AWS Key Management Service \(AWS KMS\) to use for encryption of data at rest in the ledger\. For more information, see [Encryption at rest](https://docs.aws.amazon.com/qldb/latest/developerguide/encryption-at-rest.html) in the *Amazon QLDB Developer Guide*\.  
Use one of the following options to specify this parameter:  
+  `AWS_OWNED_KMS_KEY`: Use an AWS KMS key that is owned and managed by AWS on your behalf\.
+  **Undefined**: By default, use an AWS owned KMS key\.
+  **A valid symmetric customer managed KMS key**: Use the specified symmetric encryption KMS key in your account that you create, own, and manage\.

  Amazon QLDB does not support asymmetric keys\. For more information, see [Using symmetric and asymmetric keys](https://docs.aws.amazon.com/kms/latest/developerguide/symmetric-asymmetric.html) in the * AWS Key Management Service Developer Guide*\.
To specify a customer managed KMS key, you can use its key ID, Amazon Resource Name \(ARN\), alias name, or alias ARN\. When using an alias name, prefix it with `"alias/"`\. To specify a key in a different AWS account, you must use the key ARN or alias ARN\.  
For example:  
+ Key ID: `1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Key ARN: `arn:aws:kms:us-east-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Alias name: `alias/ExampleAlias` 
+ Alias ARN: `arn:aws:kms:us-east-2:111122223333:alias/ExampleAlias` 
For more information, see [Key identifiers \(KeyId\)](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#key-id) in the * AWS Key Management Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-qldb-ledger-name"></a>
The name of the ledger that you want to create\. The name must be unique among all of the ledgers in your AWS account in the current Region\.  
Naming constraints for ledger names are defined in [Quotas in Amazon QLDB](https://docs.aws.amazon.com/qldb/latest/developerguide/limits.html#limits.naming) in the *Amazon QLDB Developer Guide*\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `(?!^.*--)(?!^[0-9]+$)(?!^-)(?!.*-$)^[A-Za-z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionsMode`  <a name="cfn-qldb-ledger-permissionsmode"></a>
The permissions mode to assign to the ledger that you want to create\. This parameter can have one of the following values:  
+  `ALLOW_ALL`: A legacy permissions mode that enables access control with API\-level granularity for ledgers\.

  This mode allows users who have the `SendCommand` API permission for this ledger to run all PartiQL commands \(hence, `ALLOW_ALL`\) on any tables in the specified ledger\. This mode disregards any table\-level or command\-level IAM permissions policies that you create for the ledger\.
+  `STANDARD`: \(*Recommended*\) A permissions mode that enables access control with finer granularity for ledgers, tables, and PartiQL commands\.

  By default, this mode denies all user requests to run any PartiQL commands on any tables in this ledger\. To allow PartiQL commands to run, you must create IAM permissions policies for specific table resources and PartiQL actions, in addition to the `SendCommand` API permission for the ledger\. For information, see [Getting started with the standard permissions mode](https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started-standard-mode.html) in the *Amazon QLDB Developer Guide*\.
We strongly recommend using the `STANDARD` permissions mode to maximize the security of your ledger data\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALLOW_ALL | STANDARD`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-qldb-ledger-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-qldb-ledger-return-values"></a>

### Ref<a name="aws-resource-qldb-ledger-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myQLDBLedger" }` 

For the resource with the logical ID `myQLDBLedger`, `Ref` returns the Amazon QLDB ledger name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-qldb-ledger--examples"></a>



### Amazon QLDB Ledger<a name="aws-resource-qldb-ledger--examples--Amazon_QLDB_Ledger"></a>

The following example describes an Amazon QLDB ledger with a `PermissionsMode` of `STANDARD` and a specified customer managed KMS key for encryption at rest\.

#### JSON<a name="aws-resource-qldb-ledger--examples--Amazon_QLDB_Ledger--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myQLDBLedger": {
      "Type": "AWS::QLDB::Ledger",
      "Properties": {
        "DeletionProtection": true,
        "KmsKey": "arn:aws:kms:us-east-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab",
        "Name": "exampleLedger",
        "PermissionsMode": "STANDARD",
        "Tags": [
          {
            "Key": "Domain",
            "Value": "Test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-qldb-ledger--examples--Amazon_QLDB_Ledger--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  myQLDBLedger: 
    Type: "AWS::QLDB::Ledger"
    Properties:
      DeletionProtection: true
      KmsKey: "arn:aws:kms:us-east-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab"
      Name: "exampleLedger"
      PermissionsMode: "STANDARD"
      Tags:
        - Key: Domain
          Value: Test
```

## See also<a name="aws-resource-qldb-ledger--seealso"></a>
+  [CreateLedger](https://docs.aws.amazon.com/qldb/latest/developerguide/API_CreateLedger.html) in the *Amazon QLDB API Reference*


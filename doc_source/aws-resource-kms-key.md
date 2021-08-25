# AWS::KMS::Key<a name="aws-resource-kms-key"></a>

The `AWS::KMS::Key` resource specifies a [symmetric or asymmetric](https://docs.aws.amazon.com/kms/latest/developerguide/symmetric-asymmetric.html) [customer master key](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys) \(CMK\) in AWS Key Management Service \(AWS KMS\)\.

You can use symmetric CMKs to encrypt and decrypt small amounts of data, but they are more commonly used to generate data keys and data key pairs\. You can also use symmetric CMKs to encrypt data stored in AWS services that are [integrated with AWS KMS](http://aws.amazon.com/kms/features/#AWS_Service_Integration)\. For more information, see [What is AWS Key Management Service?](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html) in the *AWS Key Management Service Developer Guide*\.

You can use asymmetric CMKs to encrypt and decrypt data or sign messages and verify signatures\. To create an asymmetric key, you must specify an asymmetric `KeySpec` value and a `KeyUsage` value\.

**Important**  
If you change the value of a `Replacement` property, such as `KeyUsage` or `KeySpec`, on an existing CMK, the existing CMK is [scheduled for deletion](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html) and a new CMK is created with the specified value\.  
While scheduled for deletion, the existing CMK becomes unusable\. If you don't [cancel the scheduled deletion](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html#deleting-keys-scheduling-key-deletion) of the existing CMK outside of CloudFormation, all data encrypted under the existing CMK becomes unrecoverable when the CMK is deleted\.

## Syntax<a name="aws-resource-kms-key-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kms-key-syntax.json"></a>

```
{
  "Type" : "AWS::KMS::Key",
  "Properties" : {
      "[Description](#cfn-kms-key-description)" : String,
      "[Enabled](#cfn-kms-key-enabled)" : Boolean,
      "[EnableKeyRotation](#cfn-kms-key-enablekeyrotation)" : Boolean,
      "[KeyPolicy](#cfn-kms-key-keypolicy)" : Json,
      "[KeySpec](#cfn-kms-key-keyspec)" : String,
      "[KeyUsage](#cfn-kms-key-keyusage)" : String,
      "[MultiRegion](#cfn-kms-key-multiregion)" : Boolean,
      "[PendingWindowInDays](#cfn-kms-key-pendingwindowindays)" : Integer,
      "[Tags](#cfn-kms-key-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-kms-key-syntax.yaml"></a>

```
Type: AWS::KMS::Key
Properties: 
  [Description](#cfn-kms-key-description): String
  [Enabled](#cfn-kms-key-enabled): Boolean
  [EnableKeyRotation](#cfn-kms-key-enablekeyrotation): Boolean
  [KeyPolicy](#cfn-kms-key-keypolicy): Json
  [KeySpec](#cfn-kms-key-keyspec): String
  [KeyUsage](#cfn-kms-key-keyusage): String
  [MultiRegion](#cfn-kms-key-multiregion): Boolean
  [PendingWindowInDays](#cfn-kms-key-pendingwindowindays): Integer
  [Tags](#cfn-kms-key-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-kms-key-properties"></a>

`Description`  <a name="cfn-kms-key-description"></a>
A description of the CMK\.  
Use a description that helps you decide whether the CMK is appropriate for a task\. The default value is an empty string \(no description\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-kms-key-enabled"></a>
Specifies whether the customer master key \(CMK\) is enabled\. Disabled CMKs cannot be used in cryptographic operations\.  
When `Enabled` is `true`, the *key state* of the CMK is `Enabled`\. When `Enabled` is `false`, the key state of the CMK is `Disabled`\. The default value is `true`\.  
The actual key state of the CMK might be affected by actions taken outside of CloudFormation, such as running the [EnableKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_EnableKey.html), [DisableKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_DisableKey.html), or [ScheduleKeyDeletion](https://docs.aws.amazon.com/kms/latest/APIReference/API_ScheduleKeyDeletion.html) operations\.  
For information about the key states of a CMK, see [Key state: Effect on your CMK](https://docs.aws.amazon.com/kms/latest/developerguide/key-state.html) in the *AWS Key Management Service Developer Guide*\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableKeyRotation`  <a name="cfn-kms-key-enablekeyrotation"></a>
Enables automatic rotation of the key material for the specified customer master key \(CMK\)\. By default, automation key rotation is not enabled\.  
AWS KMS does not support automatic key rotation on asymmetric CMKs\. For asymmetric CMKs, omit the `EnableKeyRotation` property or set it to `false`\.  
When you enable automatic rotation, AWS KMS automatically creates new key material for the CMK 365 days after the enable \(or reenable\) date and every 365 days thereafter\. AWS KMS retains all key material until you delete the CMK\. For detailed information about automatic key rotation, see [Rotating customer master keys](https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html) in the *AWS Key Management Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPolicy`  <a name="cfn-kms-key-keypolicy"></a>
The key policy that authorizes use of the CMK\. The key policy must conform to the following rules\.  
+ The key policy must allow the caller to make a subsequent [PutKeyPolicy](https://docs.aws.amazon.com/kms/latest/APIReference/API_PutKeyPolicy.html) request on the CMK\. This reduces the risk that the CMK becomes unmanageable\. For more information, refer to the scenario in the [Default key policy](https://docs.aws.amazon.com/kms/latest/developerguide/key-policies.html#key-policy-default-allow-root-enable-iam) section of the * *AWS Key Management Service Developer Guide* *\.
+ Each statement in the key policy must contain one or more principals\. The principals in the key policy must exist and be visible to AWS KMS\. When you create a new AWS principal \(for example, an IAM user or role\), you might need to enforce a delay before including the new principal in a key policy because the new principal might not be immediately visible to AWS KMS\. For more information, see [Changes that I make are not always immediately visible](https://docs.aws.amazon.com/IAM/latest/UserGuide/troubleshoot_general.html#troubleshoot_general_eventual-consistency) in the *AWS Identity and Access Management User Guide*\.
+ The key policy size limit is 32 kilobytes \(32768 bytes\)\.
If you are unsure of which policy to use, consider the *default key policy*\. This is the key policy that AWS KMS applies to CMKs that are created by using the CreateKey API with no specified key policy\. It gives the AWS account that owns the key permission to perform all operations on the key\. It also allows you write IAM policies to authorize access to the key\. For details, see [Default key policy](https://docs.aws.amazon.com/kms/latest/developerguide/key-policies.html#key-policy-default) in the *AWS Key Management Service Developer Guide*\.  
*Minimum*: `1`  
*Maximum*: `32768`  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeySpec`  <a name="cfn-kms-key-keyspec"></a>
Specifies the type of CMK to create\. The default value, `SYMMETRIC_DEFAULT`, creates a CMK with a 256\-bit symmetric key for encryption and decryption\. For help choosing a key spec for your CMK, see [How to Choose Your CMK Configuration](https://docs.aws.amazon.com/kms/latest/developerguide/symm-asymm-choose.html) in the *AWS Key Management Service Developer Guide*\.  
The `KeySpec` property \(`CustomerMasterKeySpec` type\) determines whether the CMK contains a symmetric key or an asymmetric key pair\. It also determines the encryption algorithms or signing algorithms that the CMK supports\. You can't change the `KeySpec` after the CMK is created\. To further restrict the algorithms that can be used with the CMK, use a condition key in its key policy or IAM policy\. For more information, see [kms:EncryptionAlgorithm](https://docs.aws.amazon.com/kms/latest/developerguide/policy-conditions.html#conditions-kms-encryption-algorithm) or [kms:Signing Algorithm](https://docs.aws.amazon.com/kms/latest/developerguide/policy-conditions.html#conditions-kms-signing-algorithm) in the *AWS Key Management Service Developer Guide*\.  
If you change the `KeySpec` of an existing CMK, the existing CMK is scheduled for deletion and a new CMK is created with the specified `KeySpec` value\. While the scheduled deletion is pending, you can't use the existing CMK\. Unless you [cancel the scheduled deletion](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html#deleting-keys-scheduling-key-deletion) of the CMK outside of CloudFormation, all data encrypted under the existing CMK becomes unrecoverable when the CMK is deleted\.
[AWS services that are integrated with AWS KMS](http://aws.amazon.com/kms/features/#AWS_Service_Integration) use symmetric CMKs to protect your data\. These services do not support asymmetric CMKs\. For help determining whether a CMK is symmetric or asymmetric, see [Identifying Symmetric and Asymmetric CMKs](https://docs.aws.amazon.com/kms/latest/developerguide/find-symm-asymm.html) in the *AWS Key Management Service Developer Guide*\.
AWS KMS supports the following key specs for CMKs:  
+ Symmetric key \(default\)
  + `SYMMETRIC_DEFAULT` \(AES\-256\-GCM\)
+ Asymmetric RSA key pairs
  + `RSA_2048`
  + `RSA_3072`
  + `RSA_4096`
+ Asymmetric NIST\-recommended elliptic curve key pairs
  + `ECC_NIST_P256` \(secp256r1\)
  + `ECC_NIST_P384` \(secp384r1\)
  + `ECC_NIST_P521` \(secp521r1\)
+ Other asymmetric elliptic curve key pairs
  + `ECC_SECG_P256K1` \(secp256k1\), commonly used for cryptocurrencies\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyUsage`  <a name="cfn-kms-key-keyusage"></a>
Determines the [cryptographic operations](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#cryptographic-operations) for which you can use the CMK\. The default value is `ENCRYPT_DECRYPT`\. This property is required only for asymmetric CMKs\. You can't change the `KeyUsage` value after the CMK is created\.  
If you change the `KeyUsage` of an existing CMK, the existing CMK is scheduled for deletion and a new CMK is created with the specified `KeyUsage` value\. While the scheduled deletion is pending, you can't use the existing CMK\. Unless you [cancel the scheduled deletion](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html#deleting-keys-scheduling-key-deletion) of the CMK outside of CloudFormation, all data encrypted under the existing CMK becomes unrecoverable when the CMK is deleted\.
Select only one valid value\.  
+ For symmetric CMKs, omit the property or specify `ENCRYPT_DECRYPT`\.
+ For asymmetric CMKs with RSA key material, specify `ENCRYPT_DECRYPT` or `SIGN_VERIFY`\.
+ For asymmetric CMKs with ECC key material, specify `SIGN_VERIFY`\.
*Required*: No  
*Type*: String  
*Allowed values*: `ENCRYPT_DECRYPT | SIGN_VERIFY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiRegion`  <a name="cfn-kms-key-multiregion"></a>
Creates a multi\-Region primary CMK that you can replicate in other AWS Regions\.  
If you change the `MultiRegion` property of an existing CMK, the existing CMK is scheduled for deletion and a new CMK is created with the specified `Multi-Region` value\. While the scheduled deletion is pending, you can't use the existing CMK\. Unless you [cancel the scheduled deletion](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html#deleting-keys-scheduling-key-deletion) of the CMK outside of CloudFormation, all data encrypted under the existing CMK becomes unrecoverable when the CMK is deleted\.
For a multi\-Region CMK, set to this property to `true`\. For a single\-Region CMK, omit this property or set it to `false`\. The default value is `false`\.  
*Multi\-Region keys* are an AWS KMS feature that lets you create multiple interoperable CMKs in different AWS Regions\. Because these CMKs have the same key ID, key material, and other metadata, you can use them to encrypt data in one AWS Region and decrypt it in a different AWS Region without making a cross\-Region call or exposing the plaintext data\. For more information, see [Using multi\-Region keys](https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html) in the *AWS Key Management Service Developer Guide*\.  
You can create a symmetric or asymmetric multi\-Region CMK, and you can create a multi\-Region CMK with imported key material\. However, you cannot create a multi\-Region CMK in a custom key store\.  
To create a replica of this primary key in a different AWS Region , create an [AWS::KMS::ReplicaKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-replicakey.html) resource in a CloudFormation stack in the replica Region\. Specify the key ARN of this primary key\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PendingWindowInDays`  <a name="cfn-kms-key-pendingwindowindays"></a>
Specifies the number of days in the waiting period before AWS KMS deletes a CMK that has been removed from a CloudFormation stack\. Enter a value between 7 and 30 days\. The default value is 30 days\.  
When you remove a customer master key \(CMK\) from a CloudFormation stack, AWS KMS schedules the CMK for deletion and starts the mandatory waiting period\. The `PendingWindowInDays` property determines the length of waiting period\. During the waiting period, the key state of CMK is `Pending Deletion` or `Pending Replica Deletion`, which prevents the CMK from being used in cryptographic operations\. When the waiting period expires, AWS KMS permanently deletes the CMK\.  
AWS KMS will not delete a [multi\-Region primary key](https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html) that has replica keys\. If you remove a multi\-Region primary key from a CloudFormation stack, its key state changes to `PendingReplicaDeletion` so it cannot be replicated or used in cryptographic operations\. This state can persist indefinitely\. When the last of its replica keys is deleted, the key state of the primary key changes to `PendingDeletion` and the waiting period specified by `PendingWindowInDays` begins\. When this waiting period expires, AWS KMS deletes the primary key\. For details, see [Deleting multi\-Region keys](https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-delete.html) in the *AWS Key Management Service Developer Guide*\.  
You cannot use a CloudFormation template to cancel deletion of the CMK after you remove it from the stack, regardless of the waiting period\. If you specify a CMK in your template, even one with the same name, CloudFormation creates a new CMK\. To cancel deletion of a CMK, use the AWS KMS console or the [CancelKeyDeletion](https://docs.aws.amazon.com/kms/latest/APIReference/API_CancelKeyDeletion.html) operation\.  
For information about the `Pending Deletion` and `Pending Replica Deletion` key states, see [Key state: Effect on your CMK](https://docs.aws.amazon.com/kms/latest/developerguide/key-state.html) in the *AWS Key Management Service Developer Guide*\. For more information about deleting CMKs, see the [ScheduleKeyDeletion](https://docs.aws.amazon.com/kms/latest/APIReference/API_ScheduleKeyDeletion.html) operation in the *AWS Key Management Service API Reference* and [Deleting customer master keys](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html) in the *AWS Key Management Service Developer Guide*\.   
*Minimum*: 7  
*Maximum*: 30  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-kms-key-tags"></a>
Assigns one or more tags to the replica key\.  
Tagging or untagging a CMK can allow or deny permission to the CMK\. For details, see [Using ABAC in AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/abac.html) in the *AWS Key Management Service Developer Guide*\.
For information about tags in AWS KMS, see [Tagging keys](https://docs.aws.amazon.com/kms/latest/developerguide/tagging-keys.html) in the *AWS Key Management Service Developer Guide*\. For information about tags in CloudFormation, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-kms-key-return-values"></a>

### Ref<a name="aws-resource-kms-key-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the key ID, such as `1234abcd-12ab-34cd-56ef-1234567890ab`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-kms-key-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-kms-key-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS customer master key \(CMK\), such as `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`\.  
For information about the key ARN of a CMK, see [Key ARN](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#key-id-key-ARN) in the *AWS Key Management Service Developer Guide*\.

`KeyId`  <a name="KeyId-fn::getatt"></a>
The key ID of the AWS KMS customer master key \(CMK\), such as `1234abcd-12ab-34cd-56ef-1234567890ab`\.  
For information about the key ID of a CMK, see [Key ID](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#key-id-key-id) in the *AWS Key Management Service Developer Guide*\.

## Examples<a name="aws-resource-kms-key--examples"></a>

### Create a symmetric CMK<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK"></a>

The following example creates a symmetric CMK\. The key policy for the CMK allows `Alice` to manage the key and allows `Bob` to view the CMK and use it in cryptographic operations\. It also allows the AWS account \(root\) full access to the key\. This prevents you from losing control of the key if both `Alice` and `Bob` are deleted from the account\.

#### JSON<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK--json"></a>

```
"myKey" : {
  "Type" : "AWS::KMS::Key",
  "Properties" : {
    "Description" : "An example symmetric CMK",
    "EnableKeyRotation": true,
    "PendingWindowInDays": 20,
    "KeyPolicy" : {
      "Version": "2012-10-17",
      "Id": "key-default-1",
      "Statement": [
        {
          "Sid": "Enable IAM User Permissions",
          "Effect": "Allow",
          "Principal": {"AWS": "arn:aws:iam::111122223333:root"},
          "Action": "kms:*",
          "Resource": "*"
        },
        {
          "Sid": "Allow administration of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::111122223333:user/Alice" },
          "Action": [
            "kms:Create*",
            "kms:Describe*",
            "kms:Enable*",
            "kms:List*",
            "kms:Put*",
            "kms:Update*",
            "kms:Revoke*",
            "kms:Disable*",
            "kms:Get*",
            "kms:Delete*",
            "kms:ScheduleKeyDeletion",
            "kms:CancelKeyDeletion"
          ],
          "Resource": "*"
        },
        {
          "Sid": "Allow use of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::111122223333:user/Bob" },
          "Action": [
            "kms:DescribeKey",
            "kms:Encrypt",
            "kms:Decrypt",
            "kms:ReEncrypt*",
            "kms:GenerateDataKey",
            "kms:GenerateDataKeyWithoutPlaintext"
          ], 
          "Resource": "*"
        }    
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK--yaml"></a>

```
myKey:
  Type: AWS::KMS::Key
  Properties:
    Description: An example symmetric CMK
    EnableKeyRotation: true
    PendingWindowInDays: 20
    KeyPolicy:
      Version: '2012-10-17'
      Id: key-default-1
      Statement:
      - Sid: Enable IAM User Permissions
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:root
        Action: kms:*
        Resource: '*'
      - Sid: Allow administration of the key
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:user/Alice
        Action:
        - kms:Create*
        - kms:Describe*
        - kms:Enable*
        - kms:List*
        - kms:Put*
        - kms:Update*
        - kms:Revoke*
        - kms:Disable*
        - kms:Get*
        - kms:Delete*
        - kms:ScheduleKeyDeletion
        - kms:CancelKeyDeletion
        Resource: '*'
      - Sid: Allow use of the key
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:user/Bob
        Action:
        - kms:DescribeKey
        - kms:Encrypt
        - kms:Decrypt
        - kms:ReEncrypt*
        - kms:GenerateDataKey
        - kms:GenerateDataKeyWithoutPlaintext
        Resource: '*'
```

### Create a symmetric CMK with a resource tag<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK_with_a_resource_tag"></a>

The following example creates a symmetric CMK with one resource tag\.

**Note**  
Tagging or untagging a CMK can allow or deny permission to the CMK\. For details, see [Using ABAC in AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/abac.html) in the *AWS Key Management Service Developer Guide*\.

#### JSON<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK_with_a_resource_tag--json"></a>

```
"myKeyWithTag" : {
      "Type" : "AWS::KMS::Key",
      "Properties" : {
        "KeyPolicy" : {
          "Version": "2012-10-17",
          "Id": "key-default-1",
          "Statement": [
            {
              "Sid": "Enable IAM User Permissions",
              "Effect": "Allow",
              "Principal": {
                "AWS": { "Fn::Join" : ["" , ["arn:aws:iam::", {"Ref" : "AWS::AccountId"} ,":root" ]] }
              },
              "Action": "kms:*",
              "Resource": "*"
            }
          ]
        },
        "Tags" : [
          {
            "Key" : {"Ref" : "Key"},
            "Value" : {"Ref" : "Value"}
          }
        ]
      }
    }
  },
  "Parameters" : {
    "Key" : {
      "Type" : "String"
    },
    "Value" : {
      "Type" : "String"
    }
  }
}
```

#### YAML<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK_with_a_resource_tag--yaml"></a>

```
myKeyWithTag:
    Type: AWS::KMS::Key
    Properties:
      KeyPolicy:
        Version: '2012-10-17'
        Id: key-default-1
        Statement:
        - Sid: Enable IAM User Permissions
          Effect: Allow
          Principal:
            AWS:
              Fn::Join:
              - ''
              - - 'arn:aws:iam::'
                - Ref: AWS::AccountId
                - :root
          Action: kms:*
          Resource: '*'
      Tags:
      - Key:
          Ref: Key
        Value:
          Ref: Value
Parameters:
  Key:
    Type: String
  Value:
    Type: String
```

### Create an asymmetric CMK<a name="aws-resource-kms-key--examples--Create_an_asymmetric_CMK"></a>

The following example creates an RSA asymmetric CMK for signing and verification\. For an asymmetric CMK, you must specify `KeySpec` and `KeyUsage` properties\. The `EnableKeyRotation` property must be omitted or set to `false`\.

#### JSON<a name="aws-resource-kms-key--examples--Create_an_asymmetric_CMK--json"></a>

```
"RSASigningKey" : {
  "Type" : "AWS::KMS::Key",
  "Properties" : {
    "Description" : "RSA-3047 asymmetric CMK for signing and verification",
    "KeySpec" : "RSA_3072",
    "KeyUsage" : "SIGN_VERIFY",
    "KeyPolicy" : {
      "Version": "2012-10-17",
      "Id": "key-default-1",
      "Statement": [
        {
          "Sid": "Enable IAM User Permissions",
          "Effect": "Allow",
          "Principal": {"AWS": "arn:aws:iam::111122223333:root"},
          "Action": "kms:*",
          "Resource": "*"
        },
        {
          "Sid": "Allow administration of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::111122223333:role/Admin" },
          "Action": [
            "kms:Create*",
            "kms:Describe*",
            "kms:Enable*",
            "kms:List*",
            "kms:Put*",
            "kms:Update*",
            "kms:Revoke*",
            "kms:Disable*",
            "kms:Get*",
            "kms:Delete*",
            "kms:ScheduleKeyDeletion",
            "kms:CancelKeyDeletion"
          ],
          "Resource": "*"
        },
        {
          "Sid": "Allow use of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::111122223333:role/Developer" },
          "Action": [
            "kms:Sign",
            "kms:Verify",
            "kms:DescribeKey"
          ], 
          "Resource": "*"
        }    
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-kms-key--examples--Create_an_asymmetric_CMK--yaml"></a>

```
RSASigningKey:
  Type: AWS::KMS::Key
  Properties:
    Description: RSA-3047 asymmetric CMK for signing and verification
    KeySpec: RSA_3072
    KeyUsage: SIGN_VERIFY
    KeyPolicy:
      Version: '2012-10-17'
      Id: key-default-1
      Statement:
      - Sid: Enable IAM User Permissions
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:root
        Action: kms:*
        Resource: '*'
      - Sid: Allow administration of the key
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:role/Admin
        Action:
        - kms:Create*
        - kms:Describe*
        - kms:Enable*
        - kms:List*
        - kms:Put*
        - kms:Update*
        - kms:Revoke*
        - kms:Disable*
        - kms:Get*
        - kms:Delete*
        - kms:ScheduleKeyDeletion
        - kms:CancelKeyDeletion
        Resource: '*'
      - Sid: Allow use of the key
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:role/Developer
        Action:        
        - kms:Sign
        - kms:Verify
        - kms:DescribeKey
        Resource: '*'
```

### Create a multi\-Region primary CMK<a name="aws-resource-kms-key--examples--Create_a_multi-Region_primary_CMK"></a>

The following example creates a multi\-Region primary CMK\.

*Multi\-Region keys* are an AWS KMS feature that lets you create multiple interoperable CMKs in different AWS Regions\. Because these CMKs have the same key ID, key material, and other metadata, you can use them to encrypt data in one AWS Region and decrypt it in a different AWS Region without making a cross\-Region call or exposing the plaintext data\. For more information, see [Using multi\-Region keys](https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html) in the *AWS Key Management Service Developer Guide*\.

To replicate this primary key into a different AWS Region, use the [AWS::KMS::ReplicaKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-replica-key.html) CloudFormation resource\.

#### JSON<a name="aws-resource-kms-key--examples--Create_a_multi-Region_primary_CMK--json"></a>

```
"myPrimaryKey" : {
  "Type" : "AWS::KMS::Key",
  "Properties" : {
    "Description" : "An example multi-Region primary key",
    "MultiRegion": true,
    "EnableKeyRotation": true,
    "PendingWindowInDays": 10,
    "KeyPolicy" : {
      "Version": "2012-10-17",
      "Id": "key-default-1",
      "Statement": [
        {
          "Sid": "Enable IAM User Permissions",
          "Effect": "Allow",
          "Principal": {"AWS": "arn:aws:iam::111122223333:root"},
          "Action": "kms:*",
          "Resource": "*"
        },
        {
          "Sid": "Allow administration of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::111122223333:user/Alice" },
          "Action": [
            "kms:ReplicateKey",
            "kms:Create*",
            "kms:Describe*",
            "kms:Enable*",
            "kms:List*",
            "kms:Put*",
            "kms:Update*",
            "kms:Revoke*",
            "kms:Disable*",
            "kms:Get*",
            "kms:Delete*",
            "kms:ScheduleKeyDeletion",
            "kms:CancelKeyDeletion"
          ],
          "Resource": "*"
        },
        {
          "Sid": "Allow use of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::111122223333:user/Bob" },
          "Action": [
            "kms:DescribeKey",
            "kms:Encrypt",
            "kms:Decrypt",
            "kms:ReEncrypt*",
            "kms:GenerateDataKey",
            "kms:GenerateDataKeyWithoutPlaintext"
          ], 
          "Resource": "*"
        }    
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-kms-key--examples--Create_a_multi-Region_primary_CMK--yaml"></a>

```
myPrimaryKey:
  Type: AWS::KMS::Key
  Properties:
    Description: An example multi-Region primary key
    MultiRegion: true
    EnableKeyRotation: true
    PendingWindowInDays 10
    KeyPolicy:
      Version: '2012-10-17'
      Id: key-default-1
      Statement:
      - Sid: Enable IAM User Permissions
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:root
        Action: kms:*
        Resource: '*'
      - Sid: Allow administration of the key
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:user/Alice
        Action:
        - kms:ReplicateKey
        - kms:Create*
        - kms:Describe*
        - kms:Enable*
        - kms:List*
        - kms:Put*
        - kms:Update*
        - kms:Revoke*
        - kms:Disable*
        - kms:Get*
        - kms:Delete*
        - kms:ScheduleKeyDeletion
        - kms:CancelKeyDeletion
        Resource: '*'
      - Sid: Allow use of the key
        Effect: Allow
        Principal:
          AWS: arn:aws:iam::111122223333:user/Bob
        Action:
        - kms:DescribeKey
        - kms:Encrypt
        - kms:Decrypt
        - kms:ReEncrypt*
        - kms:GenerateDataKey
        - kms:GenerateDataKeyWithoutPlaintext
        Resource: '*'
```

## See also<a name="aws-resource-kms-key--seealso"></a>
+  [Customer master keys](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys) in the *AWS Key Management Service Developer Guide*\.
+  [CreateKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_CreateKey.html) in the *AWS Key Management Service API Reference*\.
+  [Creating keys](https://docs.aws.amazon.com/kms/latest/developerguide/create-keys.html) in the *AWS Key Management Service Developer Guide*\.
+  [Creating multi\-Region primary keys](https://docs.aws.amazon.com/kms/latest/developerguide/create-primary-keys.html) in the *AWS Key Management Service Developer Guide*\.
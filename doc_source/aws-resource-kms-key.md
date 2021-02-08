# AWS::KMS::Key<a name="aws-resource-kms-key"></a>

The `AWS::KMS::Key` resource specifies a [symmetric or asymmetric](https://docs.aws.amazon.com/kms/latest/developerguide/symmetric-asymmetric.html) [customer master key](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys) \(CMK\) in AWS Key Management Service \(AWS KMS\)\.

You can use symmetric CMKs to encrypt and decrypt small amounts of data, but they are more commonly used to generate data keys and data key pairs\. You can also use symmetric CMKs to encrypt data stored in AWS services that are [integrated with AWS KMS](http://aws.amazon.com/kms/features/#AWS_Service_Integration)\. For more information, see [What is AWS Key Management Service?](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html) in the *AWS Key Management Service Developer Guide*\.

You can use asymmetric CMKs to encrypt and decrypt data or sign messages and verify signatures\.

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
  [PendingWindowInDays](#cfn-kms-key-pendingwindowindays): Integer
  [Tags](#cfn-kms-key-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-kms-key-properties"></a>

`Description`  <a name="cfn-kms-key-description"></a>
A description of the CMK\. Use a description that helps you to distinguish this CMK from others in the account, such as its intended use\.  
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
When you enable automatic rotation, AWS KMS automatically creates new key material for the CMK 365 days after the enable \(or reenable\) date and every 365 days thereafter\. AWS KMS retains all key material until you delete the CMK\.  
For detailed information about automatic key rotation, see [Rotating customer master keys](https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html) in the *AWS Key Management Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPolicy`  <a name="cfn-kms-key-keypolicy"></a>
The key policy that authorizes use of the CMK\. The key policy must observe the following rules\.  
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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PendingWindowInDays`  <a name="cfn-kms-key-pendingwindowindays"></a>
Specifies the number of days in the waiting period before AWS KMS deletes a CMK that has been removed from a CloudFormation stack\. Enter a value between 7 and 30 days\. The default value is 30 days\.  
When you remove a customer master key \(CMK\) from a CloudFormation stack, AWS KMS schedules the CMK for deletion and starts the mandatory waiting period\. The `PendingWindowInDays` property determines the length of waiting period\. During the waiting period, the key state of CMK is `Pending Deletion`, which prevents the CMK from being used in cryptographic operations\. When the waiting period expires, AWS KMS permanently deletes the CMK\.  
You cannot use a CloudFormation template to cancel deletion of the CMK after you remove it from the stack, regardless of the waiting period\. If you specify a CMK in your template, even one with the same name, CloudFormation creates a new CMK\. To cancel deletion of a CMK, use the AWS KMS console or the [CancelKeyDeletion](https://docs.aws.amazon.com/kms/latest/APIReference/API_CancelKeyDeletion.html) operation\.  
For information about the `PendingDeletion` key state, see [Key state: Effect on your CMK](https://docs.aws.amazon.com/kms/latest/developerguide/key-state.html) in the *AWS Key Management Service Developer Guide*\. For more information about deleting CMKs, see the [ScheduleKeyDeletion](https://docs.aws.amazon.com/kms/latest/APIReference/API_ScheduleKeyDeletion.html) operation in the *AWS Key Management Service API Reference* and [Deleting customer master keys](https://docs.aws.amazon.com/kms/latest/developerguide/deleting-keys.html) in the *AWS Key Management Service Developer Guide*\.   
*Minimum*: 7  
*Maximum*: 30  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-kms-key-tags"></a>
An array of key\-value pairs to apply to this resource\.  
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
          "Principal": { "AWS": "arn:aws:iam::123456789012:user/Alice" },
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
          "Principal": { "AWS": "arn:aws:iam::123456789012:user/Bob" },
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
          AWS: arn:aws:iam::123456789012:user/Alice
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
          AWS: arn:aws:iam::123456789012:user/Bob
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

#### JSON<a name="aws-resource-kms-key--examples--Create_a_symmetric_CMK_with_a_resource_tag--json"></a>

```
{
  "Resources" : {
    "myKey" : {
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
Resources:
  myKey:
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

## See also<a name="aws-resource-kms-key--seealso"></a>
+  [Creating keys](https://docs.aws.amazon.com/kms/latest/developerguide/create-keys.html) in the *AWS Key Management Service Developer Guide*\.
+  [CreateKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_CreateKey.html) in the *AWS Key Management Service API Reference*\.
+  [Customer master keys](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys) in the *AWS Key Management Service Developer Guide*\.


# AWS::KMS::Alias<a name="aws-resource-kms-alias"></a>

The `AWS::KMS::Alias` resource specifies a display name for a [KMS key](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#kms_keys)\. You can use an alias to identify a KMS key in the AWS KMS console, in the [DescribeKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_DescribeKey.html) operation, and in [cryptographic operations](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#cryptographic-operations), such as [Decrypt](https://docs.aws.amazon.com/kms/latest/APIReference/API_Decrypt.html) and [GenerateDataKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_GenerateDataKey.html)\.

**Note**  
Adding, deleting, or updating an alias can allow or deny permission to the KMS key\. For details, see [ABAC for AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/abac.html) in the *AWS Key Management Service Developer Guide*\.

Using an alias to refer to a KMS key can help you simplify key management\. For example, an alias in your code can be associated with different KMS keys in different AWS Regions\. For more information, see [Using aliases](https://docs.aws.amazon.com/kms/latest/developerguide/kms-alias.html) in the *AWS Key Management Service Developer Guide*\.

When specifying an alias, observe the following rules\.
+ Each alias is associated with one KMS key, but multiple aliases can be associated with the same KMS key\.
+ The alias and its associated KMS key must be in the same AWS account and Region\.
+ The alias name must be unique in the AWS account and Region\. However, you can create aliases with the same name in different AWS Regions\. For example, you can have an `alias/projectKey` in multiple Regions, each of which is associated with a KMS key in its Region\.
+ Each alias name must begin with `alias/` followed by a name, such as `alias/exampleKey`\. The alias name can contain only alphanumeric characters, forward slashes \(/\), underscores \(\_\), and dashes \(\-\)\. Alias names cannot begin with `alias/aws/`\. That alias name prefix is reserved for [AWS managed keys](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#aws-managed-cmk)\.

**Regions**

AWS KMS CloudFormation resources are available in all AWS Regions in which AWS KMS and AWS CloudFormation are supported\.

## Syntax<a name="aws-resource-kms-alias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kms-alias-syntax.json"></a>

```
{
  "Type" : "AWS::KMS::Alias",
  "Properties" : {
      "[AliasName](#cfn-kms-alias-aliasname)" : String,
      "[TargetKeyId](#cfn-kms-alias-targetkeyid)" : String
    }
}
```

### YAML<a name="aws-resource-kms-alias-syntax.yaml"></a>

```
Type: AWS::KMS::Alias
Properties: 
  [AliasName](#cfn-kms-alias-aliasname): String
  [TargetKeyId](#cfn-kms-alias-targetkeyid): String
```

## Properties<a name="aws-resource-kms-alias-properties"></a>

`AliasName`  <a name="cfn-kms-alias-aliasname"></a>
Specifies the alias name\. This value must begin with `alias/` followed by a name, such as `alias/ExampleAlias`\.   
If you change the value of the `AliasName` property, the existing alias is deleted and a new alias is created for the specified KMS key\. This change can disrupt applications that use the alias\. It can also allow or deny access to a KMS key affected by attribute\-based access control \(ABAC\)\.
The alias must be string of 1\-256 characters\. It can contain only alphanumeric characters, forward slashes \(/\), underscores \(\_\), and dashes \(\-\)\. The alias name cannot begin with `alias/aws/`\. The `alias/aws/` prefix is reserved for [AWS managed keys](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#aws-managed-cmk)\.  
*Pattern*: `^alias/[a-zA-Z0-9/_-]+$`  
*Minimum*: `1`  
*Maximum*: `256`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetKeyId`  <a name="cfn-kms-alias-targetkeyid"></a>
Associates the alias with the specified [customer managed key](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#customer-cmk)\. The KMS key must be in the same AWS account and Region\.  
A valid key ID is required\. If you supply a null or empty string value, this operation returns an error\.  
For help finding the key ID and ARN, see [Finding the key ID and ARN](https://docs.aws.amazon.com/kms/latest/developerguide/viewing-keys.html#find-cmk-id-arn) in the *AWS Key Management Service Developer Guide*\.  
Specify the key ID or the key ARN of the KMS key\.  
For example:  
+ Key ID: `1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Key ARN: `arn:aws:kms:us-east-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab` 
To get the key ID and key ARN for a KMS key, use [ListKeys](https://docs.aws.amazon.com/kms/latest/APIReference/API_ListKeys.html) or [DescribeKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_DescribeKey.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-kms-alias-return-values"></a>

### Ref<a name="aws-resource-kms-alias-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the alias name, such as `alias/exampleAlias`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-kms-alias--examples"></a>

### Create an alias<a name="aws-resource-kms-alias--examples--Create_an_alias"></a>

The following examples create the `alias/exampleAlias` alias for a KMS key\. The KMS key is identified by a reference to its CloudFormation resource name\. Before using these examples, replace the example target key ID and example alias with valid values\.

#### JSON<a name="aws-resource-kms-alias--examples--Create_an_alias--json"></a>

```
{
    "myAlias": {
        "Type": "AWS::KMS::Alias",
        "Properties": {
            "AliasName": "alias/exampleAlias",
            "TargetKeyId": {
                "Ref": "myKey"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-kms-alias--examples--Create_an_alias--yaml"></a>

```
myAlias:
  Type: 'AWS::KMS::Alias'
  Properties:
    AliasName: alias/exampleAlias
    TargetKeyId: !Ref myKey
```

## See also<a name="aws-resource-kms-alias--seealso"></a>
+  [CreateAlias](https://docs.aws.amazon.com/kms/latest/APIReference/API_CreateAlias.html) in the *AWS Key Management Service API Reference*\.
+  [Using aliases](https://docs.aws.amazon.com/kms/latest/developerguide/kms-alias.html) in the *AWS Key Management Service Developer Guide*\.
+  [ABAC for AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/abac.html) in the *AWS Key Management Service Developer Guide*\.


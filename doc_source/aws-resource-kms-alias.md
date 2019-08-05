# AWS::KMS::Alias<a name="aws-resource-kms-alias"></a>

The `AWS::KMS::Alias` resource specifies a display name for a [customer master key](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys) \(CMK\) in AWS Key Management Service \(AWS KMS\)\. You can use an alias to identify a CMK in cryptographic operations\.

Using an alias to refer to a CMK can help you simplify key management\. For example, an alias in your code can map to different CMKs in different AWS Regions\. For more information, see [Working with Aliases](https://docs.aws.amazon.com/kms/latest/developerguide/programming-aliases.html) in the *AWS Key Management Service Developer Guide*\.

When specifying an alias, observe the following rules\.
+ Each alias can point to only one CMK, but multiple aliases can point to the same CMK\.
+ The alias and the CMK it points to must be in the same AWS account and Region\.
+ The alias name must be unique in the AWS account and Region\. However, you can create aliases with the same name in different AWS Regions\. For example, you can have an `alias/projectKey` in multiple Regions, each of which points to a CMK in that Region\.
+ Each alias name must begin with `alias/` followed by a name, such as `alias/exampleKey`\. The alias name can contain only alphanumeric characters, forward slashes \(/\), underscores \(\_\), and dashes \(\-\)\. Alias names cannot begin with **alias/aws/**\. That alias name prefix is reserved for [AWS managed CMKs](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#aws-managed-cmk)\.

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
Specifies the alias name\. This value must begin with `alias/` followed by a name, such as `alias/ExampleAlias`\. The alias name cannot begin with `alias/aws/`\. The `alias/aws/` prefix is reserved for AWS managed CMKs\.
*Required*: Yes
*Type*: String
*Minimum*: `1`
*Maximum*: `256`
*Pattern*: `^[a-zA-Z0-9:/_-]+$`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetKeyId`  <a name="cfn-kms-alias-targetkeyid"></a>
Identifies the CMK to which the alias refers\. Specify the key ID or the Amazon Resource Name \(ARN\) of the CMK\. You cannot specify another alias\. For help finding the key ID and ARN, see [Finding the Key ID and ARN](https://docs.aws.amazon.com/kms/latest/developerguide/viewing-keys.html#find-cmk-id-arn) in the *AWS Key Management Service Developer Guide*\.
*Required*: Yes
*Type*: String
*Minimum*: `1`
*Maximum*: `2048`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-kms-alias-return-values"></a>

### Ref<a name="aws-resource-kms-alias-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the alias name, such as `alias/exampleAlias`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-kms-alias--examples"></a>

### Create an alias<a name="aws-resource-kms-alias--examples--Create_an_alias"></a>

The following examples create the `alias/exampleAlias` alias for a CMK\. The CMK is identified by referencing its resource name\. Before using these examples, replace the example target key ID with a valid value\.

#### JSON<a name="aws-resource-kms-alias--examples--Create_an_alias--json"></a>

```
"myAlias" : {
  "Type" : "AWS::KMS::Alias",
  "Properties" : {
    "AliasName" : "alias/exampleAlias",
    "TargetKeyId" : {"Ref": "myKey"}
  }
}
```

#### YAML<a name="aws-resource-kms-alias--examples--Create_an_alias--yaml"></a>

```
myAlias:
  Type: AWS::KMS::Alias
  Properties:
    AliasName: alias/exampleAlias
    TargetKeyId:
      Ref: myKey
```

## See Also<a name="aws-resource-kms-alias--seealso"></a>
+  [CreateAlias](https://docs.aws.amazon.com/kms/latest/APIReference/API_CreateAlias.html) in the *AWS Key Management Service API Reference*\.

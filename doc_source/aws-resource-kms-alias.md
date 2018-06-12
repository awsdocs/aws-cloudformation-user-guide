# AWS::KMS::Alias<a name="aws-resource-kms-alias"></a>

The `AWS::KMS::Alias` resource creates a display name for a customer master key \(CMK\) in AWS Key Management Service \(AWS KMS\)\. Using an alias to refer to a key can help you simplify key management\. For example, when rotating keys, you can just update the alias mapping instead of tracking and changing key IDs\. For more information, see [Working with Aliases](http://docs.aws.amazon.com/kms/latest/developerguide/programming-aliases.html) in the *AWS Key Management Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-kms-alias-syntax)
+ [Properties](#aws-resource-kms-alias-properties)
+ [Return Value](#aws-resource-kms-alias-returnvalues)
+ [Examples](#aws-resource-kms-alias-examples)

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
Type: "AWS::KMS::Alias"
Properties:
  [AliasName](#cfn-kms-alias-aliasname): String
  [TargetKeyId](#cfn-kms-alias-targetkeyid): String
```

## Properties<a name="aws-resource-kms-alias-properties"></a>

`AliasName`  <a name="cfn-kms-alias-aliasname"></a>
The name of the alias\. The name must start with `alias` followed by a forward slash, such as `alias/`\. You can't specify aliases that begin with `alias/AWS`\. These aliases are reserved\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TargetKeyId`  <a name="cfn-kms-alias-targetkeyid"></a>
The ID of the key for which you are creating the alias\. Specify the key's globally unique identifier or Amazon Resource Name \(ARN\)\. You can't specify another alias\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-kms-alias-returnvalues"></a>

### Ref<a name="w3ab2c21c10d839c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the alias name, such as `alias/myKeyAlias`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-kms-alias-examples"></a>

The following examples create the `alias/myKeyAlias` alias for the `myKey` AWS KMS key\.

### JSON<a name="aws-resource-kms-alias-examples.json"></a>

```
"myKeyAlias" : {
  "Type" : "AWS::KMS::Alias",
  "Properties" : {
    "AliasName" : "alias/myKeyAlias",
    "TargetKeyId" : {"Ref":"myKey"}
  }
}
```

### YAML<a name="aws-resource-kms-alias-examples.yaml"></a>

```
myKeyAlias:
  Type: AWS::KMS::Alias
  Properties:
    AliasName: alias/myKeyAlias
    TargetKeyId:
      Ref: myKey
```
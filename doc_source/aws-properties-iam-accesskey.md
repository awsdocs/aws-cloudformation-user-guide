# AWS::IAM::AccessKey<a name="aws-properties-iam-accesskey"></a>

The AWS::IAM::AccessKey resource type generates a secret access key and assigns it to an IAM user or AWS account\.

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

**Topics**
+ [Syntax](#aws-resource-iam-accesskey-syntax)
+ [Properties](#aws-properties-iam-accesskey-prop)
+ [Return Values](#aws-properties-iam-accesskey-ref)
+ [Template Examples](#w3ab2c21c10d745c15)

## Syntax<a name="aws-resource-iam-accesskey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-accesskey-syntax.json"></a>

```
{
   "Type": "AWS::IAM::AccessKey",
   "Properties": {
      "[Serial](#cfn-iam-accesskey-serial)": Integer,
      "[Status](#cfn-iam-accesskey-status)": String,
      "[UserName](#cfn-iam-accesskey-username)": String
   }
}
```

### YAML<a name="aws-resource-iam-accesskey-syntax.yaml"></a>

```
Type: "AWS::IAM::AccessKey"
Properties: 
  [Serial](#cfn-iam-accesskey-serial): Integer
  [Status](#cfn-iam-accesskey-status): String
  [UserName](#cfn-iam-accesskey-username): String
```

## Properties<a name="aws-properties-iam-accesskey-prop"></a>

`Serial`  <a name="cfn-iam-accesskey-serial"></a>
This value is specific to AWS CloudFormation and can only be *incremented*\. Incrementing this value notifies AWS CloudFormation that you want to rotate your access key\. When you update your stack, AWS CloudFormation will replace the existing access key with a new key\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Status`  <a name="cfn-iam-accesskey-status"></a>
The status of the access key\. By default, AWS CloudFormation sets this property value to `Active`\.  
*Required*: No  
*Type*: String  
*Valid values:* `Active` or `Inactive`  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UserName`  <a name="cfn-iam-accesskey-username"></a>
The name of the user that the new key will belong to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-properties-iam-accesskey-ref"></a>

### Ref<a name="w3ab2c21c10d745c13b2"></a>

Specifying this resource ID to the intrinsic `Ref` function will return the `AccessKeyId`\. For example: `AKIAIOSFODNN7EXAMPLE`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d745c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`SecretAccessKey`  
Returns the secret access key for the specified `AWS::IAM::AccessKey` resource\. For example: `wJalrXUtnFEMI/K7MDENG/bPxRfiCYzEXAMPLEKEY`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Template Examples<a name="w3ab2c21c10d745c15"></a>

To view AWS::IAM::AccessKey snippets, see [Declaring an IAM Access Key Resource](quickref-iam.md#scenario-iam-accesskey)\.
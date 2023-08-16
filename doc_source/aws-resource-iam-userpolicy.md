# AWS::IAM::UserPolicy<a name="aws-resource-iam-userpolicy"></a>

Adds or updates an inline policy document that is embedded in the specified IAM user\.

An IAM user can also have a managed policy attached to it\. To attach a managed policy to a user, use [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)\. To create a new managed policy, use [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-managedpolicy.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-managedpolicy.html)\. For information about policies, see [Managed policies and inline policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *IAM User Guide*\.

For information about the maximum number of inline policies that you can embed in a user, see [IAM and AWS STS quotas](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-userpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-userpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::UserPolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-iam-userpolicy-policydocument)" : Json,
      "[PolicyName](#cfn-iam-userpolicy-policyname)" : String,
      "[UserName](#cfn-iam-userpolicy-username)" : String
    }
}
```

### YAML<a name="aws-resource-iam-userpolicy-syntax.yaml"></a>

```
Type: AWS::IAM::UserPolicy
Properties: 
  [PolicyDocument](#cfn-iam-userpolicy-policydocument): Json
  [PolicyName](#cfn-iam-userpolicy-policyname): String
  [UserName](#cfn-iam-userpolicy-username): String
```

## Properties<a name="aws-resource-iam-userpolicy-properties"></a>

`PolicyDocument`  <a name="cfn-iam-userpolicy-policydocument"></a>
The policy document\.  
You must provide policies in JSON format in IAM\. However, for AWS CloudFormation templates formatted in YAML, you can provide the policy in JSON or YAML format\. AWS CloudFormation always converts a YAML policy to JSON format before submitting it to IAM\.  
The [regex pattern](http://wikipedia.org/wiki/regex) used to validate this parameter is a string of characters consisting of the following:  
+ Any printable ASCII character ranging from the space character \(`\u0020`\) through the end of the ASCII character range
+ The printable characters in the Basic Latin and Latin\-1 Supplement character set \(through `\u00FF`\)
+ The special characters tab \(`\u0009`\), line feed \(`\u000A`\), and carriage return \(`\u000D`\)
*Required*: No  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `131072`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-iam-userpolicy-policyname"></a>
The name of the policy document\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserName`  <a name="cfn-iam-userpolicy-username"></a>
The name of the user to associate the policy with\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iam-userpolicy-return-values"></a>

### Ref<a name="aws-resource-iam-userpolicy-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref`intrinsic function, `Ref`returns the resource name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iam-userpolicy--examples"></a>



### IAM user embedded inline policy document<a name="aws-resource-iam-userpolicy--examples--_user_embedded_inline_policy_document"></a>

This example shows an inline policy document in `AWS::IAM::UserPolicy`\. The policy will be embedded in the specified IAM user, `RootUser`\.

#### JSON<a name="aws-resource-iam-userpolicy--examples--_user_embedded_inline_policy_document--json"></a>

```
{
    "Type": "AWS::IAM::UserPolicy",
    "Properties": {
        "PolicyName": "root",
        "PolicyDocument": {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": "*",
                    "Resource": "*"
                }
            ]
        },
        "UserName": "RootUser"
    }
}
```

#### YAML<a name="aws-resource-iam-userpolicy--examples--_user_embedded_inline_policy_document--yaml"></a>

```
Type: 'AWS::IAM::UserPolicy'
Properties:
  PolicyName: root
  PolicyDocument:
    Version: "2012-10-17"
    Statement:
      - Effect: Allow
        Action: '*'
        Resource: '*'
  UserName: RootUser
```

### IAM user embedded inline policy document with Ref function<a name="aws-resource-iam-userpolicy--examples--_user_embedded_inline_policy_document_with_Ref_function"></a>

This example shows an inline policy document in `AWS::IAM::UserPolicy`\. The example uses the `Ref` function in the `UserName` property to specify the logical ID of a `AWS::IAM::User` resource\. For the logical ID of the `AWS::IAM::User` resource, `Ref` returns the user name\.

#### JSON<a name="aws-resource-iam-userpolicy--examples--_user_embedded_inline_policy_document_with_Ref_function--json"></a>

```
{
    "Type": "AWS::IAM::UserPolicy",
    "Properties": {
        "PolicyName": "root",
        "PolicyDocument": {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": "*",
                    "Resource": "*"
                }
            ]
        },
        "UserName": {
            "Ref": "RootUser"
        }
    }
}
```

#### YAML<a name="aws-resource-iam-userpolicy--examples--_user_embedded_inline_policy_document_with_Ref_function--yaml"></a>

```
Type: 'AWS::IAM::UserPolicy'
Properties:
  PolicyName: root
  PolicyDocument:
    Version: "2012-10-17"
    Statement:
      - Effect: Allow
        Action: '*'
        Resource: '*'
  UserName: !Ref RootUser
```

## See also<a name="aws-resource-iam-userpolicy--seealso"></a>
+  [PutUserPolicy](https://docs.aws.amazon.com/IAM/latest/APIReference/API_PutUserPolicy.html) in the *AWS Identity and Access Management API Reference* 
+  [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html) 


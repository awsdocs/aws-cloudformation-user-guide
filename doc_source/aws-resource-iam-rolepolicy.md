# AWS::IAM::RolePolicy<a name="aws-resource-iam-rolepolicy"></a>

Adds or updates an inline policy document that is embedded in the specified IAM role\.

When you embed an inline policy in a role, the inline policy is used as part of the role's access \(permissions\) policy\. The role's trust policy is created at the same time as the role, using [https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateRole.html](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateRole.html)\. You can update a role's trust policy using [https://docs.aws.amazon.com/IAM/latest/APIReference/API_UpdateAssumeRolePolicy.html](https://docs.aws.amazon.com/IAM/latest/APIReference/API_UpdateAssumeRolePolicy.html)\. For information about roles, see [IAM roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/roles-toplevel.html) in the *IAM User Guide*\.

A role can also have a managed policy attached to it\. To attach a managed policy to a role, use [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)\. To create a new managed policy, use [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-managedpolicy.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-managedpolicy.html)\. For information about policies, see [Managed policies and inline policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *IAM User Guide*\.

For information about the maximum number of inline policies that you can embed with a role, see [IAM and AWS STS quotas](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-rolepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-rolepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::RolePolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-iam-rolepolicy-policydocument)" : Json,
      "[PolicyName](#cfn-iam-rolepolicy-policyname)" : String,
      "[RoleName](#cfn-iam-rolepolicy-rolename)" : String
    }
}
```

### YAML<a name="aws-resource-iam-rolepolicy-syntax.yaml"></a>

```
Type: AWS::IAM::RolePolicy
Properties: 
  [PolicyDocument](#cfn-iam-rolepolicy-policydocument): Json
  [PolicyName](#cfn-iam-rolepolicy-policyname): String
  [RoleName](#cfn-iam-rolepolicy-rolename): String
```

## Properties<a name="aws-resource-iam-rolepolicy-properties"></a>

`PolicyDocument`  <a name="cfn-iam-rolepolicy-policydocument"></a>
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

`PolicyName`  <a name="cfn-iam-rolepolicy-policyname"></a>
The name of the policy document\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleName`  <a name="cfn-iam-rolepolicy-rolename"></a>
The name of the role to associate the policy with\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iam-rolepolicy-return-values"></a>

### Ref<a name="aws-resource-iam-rolepolicy-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref`intrinsic function, `Ref`returns the resource name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iam-rolepolicy--examples"></a>



### IAM role embedded inline policy document<a name="aws-resource-iam-rolepolicy--examples--_role_embedded_inline_policy_document"></a>

This example shows an inline policy document in `AWS::IAM::RolePolicy`\. The policy will be embedded in the specified IAM role, `RootRole`\.

#### JSON<a name="aws-resource-iam-rolepolicy--examples--_role_embedded_inline_policy_document--json"></a>

```
{
    "Type": "AWS::IAM::RolePolicy",
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
        "RoleName": "RootRole"
    }
}
```

#### YAML<a name="aws-resource-iam-rolepolicy--examples--_role_embedded_inline_policy_document--yaml"></a>

```
Type: 'AWS::IAM::RolePolicy'
Properties:
  PolicyName: root
  PolicyDocument:
    Version: "2012-10-17"
    Statement:
      - Effect: Allow
        Action: '*'
        Resource: '*'
  RoleName: RootRole
```

### IAM role embedded inline policy document with Ref function<a name="aws-resource-iam-rolepolicy--examples--_role_embedded_inline_policy_document_with_Ref_function"></a>

This example shows an inline policy document in `AWS::IAM::RolePolicy`\. The example uses the `Ref` function in the `RoleName` property to specify the logical ID of a `AWS::IAM::Role` resource\. For the logical ID of the `AWS::IAM::Role` resource, `Ref` returns the role name\.

#### JSON<a name="aws-resource-iam-rolepolicy--examples--_role_embedded_inline_policy_document_with_Ref_function--json"></a>

```
{
    "Type": "AWS::IAM::RolePolicy",
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
        "RoleName": {
            "Ref": "RootRole"
        }
    }
}
```

#### YAML<a name="aws-resource-iam-rolepolicy--examples--_role_embedded_inline_policy_document_with_Ref_function--yaml"></a>

```
Type: 'AWS::IAM::RolePolicy'
Properties:
  PolicyName: root
  PolicyDocument:
    Version: "2012-10-17"
    Statement:
      - Effect: Allow
        Action: '*'
        Resource: '*'
  RoleName: !Ref RootRole
```

## See also<a name="aws-resource-iam-rolepolicy--seealso"></a>
+  [PutRolePolicy](https://docs.aws.amazon.com/IAM/latest/APIReference/API_PutRolePolicy.html) in the *AWS Identity and Access Management API Reference* 
+  [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html) 


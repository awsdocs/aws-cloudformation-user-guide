# AWS::IAM::Policy<a name="aws-resource-iam-policy"></a>

Adds or updates an inline policy document that is embedded in the specified IAM user, group, or role\.

An IAM user can also have a managed policy attached to it\. For information about policies, see [Managed Policies and Inline Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *IAM User Guide*\.

The Groups, Roles, and Users properties are optional\. However, you must specify at least one of these properties\.

For information about limits on the number of inline policies that you can embed in an identity, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-policy-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::Policy",
  "Properties" : {
      "[Groups](#cfn-iam-policy-groups)" : [ String, ... ],
      "[PolicyDocument](#cfn-iam-policy-policydocument)" : Json,
      "[PolicyName](#cfn-iam-policy-policyname)" : String,
      "[Roles](#cfn-iam-policy-roles)" : [ String, ... ],
      "[Users](#cfn-iam-policy-users)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-iam-policy-syntax.yaml"></a>

```
Type: AWS::IAM::Policy
Properties: 
  [Groups](#cfn-iam-policy-groups): 
    - String
  [PolicyDocument](#cfn-iam-policy-policydocument): Json
  [PolicyName](#cfn-iam-policy-policyname): String
  [Roles](#cfn-iam-policy-roles): 
    - String
  [Users](#cfn-iam-policy-users): 
    - String
```

## Properties<a name="aws-resource-iam-policy-properties"></a>

`Groups`  <a name="cfn-iam-policy-groups"></a>
The name of the group to associate the policy with\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-\.  
*Required*: No  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDocument`  <a name="cfn-iam-policy-policydocument"></a>
The policy document\.  
You must provide policies in JSON format in IAM\. However, for AWS CloudFormation templates formatted in YAML, you can provide the policy in JSON or YAML format\. AWS CloudFormation always converts a YAML policy to JSON format before submitting it to IAM\.  
The [regex pattern](http://wikipedia.org/wiki/regex) used to validate this parameter is a string of characters consisting of the following:  
+ Any printable ASCII character ranging from the space character \(`\u0020`\) through the end of the ASCII character range
+ The printable characters in the Basic Latin and Latin\-1 Supplement character set \(through `\u00FF`\)
+ The special characters tab \(`\u0009`\), line feed \(`\u000A`\), and carriage return \(`\u000D`\)
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `131072`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-iam-policy-policyname"></a>
The name of the policy document\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Roles`  <a name="cfn-iam-policy-roles"></a>
The name of the role to associate the policy with\.  
This parameter allows \(per its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
If an external policy \(such as `AWS::IAM::Policy` or `AWS::IAM::ManagedPolicy`\) has a `Ref` to a role and if a resource \(such as `AWS::ECS::Service`\) also has a `Ref` to the same role, add a `DependsOn` attribute to the resource to make the resource depend on the external policy\. This dependency ensures that the role's policy is available throughout the resource's lifecycle\. For example, when you delete a stack with an `AWS::ECS::Service` resource, the `DependsOn` attribute ensures that AWS CloudFormation deletes the `AWS::ECS::Service` resource before deleting its role's policy\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Users`  <a name="cfn-iam-policy-users"></a>
The name of the user to associate the policy with\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-policy-return-values"></a>

### Ref<a name="aws-resource-iam-policy-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iam-policy--examples"></a>



### IAM Policy with policy group<a name="aws-resource-iam-policy--examples--IAM_Policy_with_policy_group"></a>

#### JSON<a name="aws-resource-iam-policy--examples--IAM_Policy_with_policy_group--json"></a>

```
{
    "Type": "AWS::IAM::Policy",
    "Properties": {
        "PolicyName": "CFNUsers",
        "PolicyDocument": {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": [
                        "cloudformation:Describe*",
                        "cloudformation:List*",
                        "cloudformation:Get*"
                    ],
                    "Resource": "*"
                }
            ]
        },
        "Groups": [
            {
                "Ref": "CFNUserGroup"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-iam-policy--examples--IAM_Policy_with_policy_group--yaml"></a>

```
Type: 'AWS::IAM::Policy'
Properties:
  PolicyName: CFNUsers
  PolicyDocument:
    Version: 2012-10-17
    Statement:
      - Effect: Allow
        Action:
          - 'cloudformation:Describe*'
          - 'cloudformation:List*'
          - 'cloudformation:Get*'
        Resource: '*'
  Groups:
    - !Ref CFNUserGroup
```

### IAM Policy with specified role<a name="aws-resource-iam-policy--examples--IAM_Policy_with_specified_role"></a>

#### JSON<a name="aws-resource-iam-policy--examples--IAM_Policy_with_specified_role--json"></a>

```
{
    "Type": "AWS::IAM::Policy",
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
        "Roles": [
            {
                "Ref": "RootRole"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-iam-policy--examples--IAM_Policy_with_specified_role--yaml"></a>

```
Type: 'AWS::IAM::Policy'
Properties:
  PolicyName: root
  PolicyDocument:
    Version: 2012-10-17
    Statement:
      - Effect: Allow
        Action: '*'
        Resource: '*'
  Roles:
    - !Ref RootRole
```

## See also<a name="aws-resource-iam-policy--seealso"></a>
+  [CreatePolicy](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreatePolicy.html) in the *AWS Identity and Access Management API Reference* 


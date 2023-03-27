# AWS::IAM::Role Policy<a name="aws-properties-iam-policy-1"></a>

Contains information about an attached policy\.

An attached policy is a managed policy that has been attached to a user, group, or role\.

For more information about managed policies, refer to [Managed Policies and Inline Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *IAM User Guide*\. 

## Syntax<a name="aws-properties-iam-policy-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-policy-1-syntax.json"></a>

```
{
  "[PolicyDocument](#cfn-iam-policies-policydocument)" : Json,
  "[PolicyName](#cfn-iam-policies-policyname)" : String
}
```

### YAML<a name="aws-properties-iam-policy-1-syntax.yaml"></a>

```
  [PolicyDocument](#cfn-iam-policies-policydocument): Json
  [PolicyName](#cfn-iam-policies-policyname): String
```

## Properties<a name="aws-properties-iam-policy-1-properties"></a>

`PolicyDocument`  <a name="cfn-iam-policies-policydocument"></a>
The entire contents of the policy that defines permissions\. For more information, see [Overview of JSON policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html#access_policies-json)\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-iam-policies-policyname"></a>
The friendly name \(not ARN\) identifying the policy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-iam-policy-1--examples"></a>

### IAM Role Policy<a name="aws-properties-iam-policy-1--examples--_Role_Policy"></a>

This example shows how the policy document is declared\.

#### JSON<a name="aws-properties-iam-policy-1--examples--_Role_Policy--json"></a>

```
{
    "PolicyName": "root",
    "PolicyDocument": {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Sid": "IamListAccess",
                "Effect": "Allow",
                "Action": [
                    "iam:ListRoles",
                    "iam:ListUsers"
                ],
                "Resource": "*"
            }
        ]
    }
}
```

#### YAML<a name="aws-properties-iam-policy-1--examples--_Role_Policy--yaml"></a>

```
PolicyName: root
PolicyDocument:
   Version: 2012-10-17
   Statement:
      - Sid: IamListAccess
        Effect: Allow
        Action:
          - 'iam:ListRoles'
          - 'iam:ListUsers'
        Resource: '*'
```

## See also<a name="aws-properties-iam-policy-1--seealso"></a>
+  [PolicyDetail](https://docs.aws.amazon.com/IAM/latest/APIReference/API_PolicyDetail.html) in the *AWS Identity and Access Management API Reference* 


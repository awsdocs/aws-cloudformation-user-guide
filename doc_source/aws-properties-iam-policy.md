# AWS::IAM::Role Policy<a name="aws-properties-iam-policy"></a>

Contains information about an attached policy\.

An attached policy is a managed policy that has been attached to a user, group, or role\.

For more information about managed policies, refer to [Managed Policies and Inline Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *Using IAM* guide\. 

## Syntax<a name="aws-properties-iam-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-policy-syntax.json"></a>

```
{
  "[PolicyDocument](#cfn-iam-policies-policydocument)" : Json,
  "[PolicyName](#cfn-iam-policies-policyname)" : String
}
```

### YAML<a name="aws-properties-iam-policy-syntax.yaml"></a>

```
  [PolicyDocument](#cfn-iam-policies-policydocument): Json
  [PolicyName](#cfn-iam-policies-policyname): String
```

## Properties<a name="aws-properties-iam-policy-properties"></a>

`PolicyDocument`  <a name="cfn-iam-policies-policydocument"></a>
The policy document\.  
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `131072`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-iam-policies-policyname"></a>
The friendly name \(not ARN\) identifying the policy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-iam-policy--seealso"></a>
+  [PolicyDetail](https://docs.aws.amazon.com/IAM/latest/APIReference/API_PolicyDetail.html) in the *AWS Identity and Access Management API Reference* 


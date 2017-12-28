# IAM Policies<a name="aws-properties-iam-policy"></a>

`Policies` is a property of the [AWS::IAM::Role](aws-resource-iam-role.md), [AWS::IAM::Group](aws-properties-iam-group.md), and [AWS::IAM::User](aws-properties-iam-user.md) resources\. The `Policies` property describes what actions are allowed on what resources\. For more information about IAM policies, see [Overview of Policies](http://docs.aws.amazon.com/IAM/latest/UserGuide/PoliciesOverview.html) and [AWS IAM Policy Reference](http://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies.html) in the *IAM User Guide*\.

## Syntax<a name="w3ab2c21c14e1111b5"></a>

### JSON<a name="aws-properties-iam-policy-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-policies-policydocument)" : JSON,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-policies-policyname)" : String
}
```

### YAML<a name="aws-properties-iam-policy-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-policies-policydocument): JSON
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-policies-policyname): String
```

## Properties<a name="w3ab2c21c14e1111b7"></a>

`PolicyDocument`  
A policy document that describes what actions are allowed on which resources\.  
*Required: *Yes  
*Type*: JSON object  
*Update requires*: No interruption

`PolicyName`  
The name of the policy\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption
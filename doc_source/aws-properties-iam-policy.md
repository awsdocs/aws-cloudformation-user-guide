# IAM Policies<a name="aws-properties-iam-policy"></a>

`Policies` is a property of the [AWS::IAM::Role](aws-resource-iam-role.md), [AWS::IAM::Group](aws-properties-iam-group.md), and [AWS::IAM::User](aws-properties-iam-user.md) resources\. The `Policies` property describes what actions are allowed on what resources\. For more information about IAM policies, see [Overview of Policies](http://docs.aws.amazon.com/IAM/latest/UserGuide/PoliciesOverview.html) and [AWS IAM Policy Reference](http://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies.html) in the *IAM User Guide*\.

## Syntax<a name="w3ab2c21c14e1308b5"></a>

### JSON<a name="aws-properties-iam-policy-syntax.json"></a>

```
{
  "[PolicyDocument](#cfn-iam-policies-policydocument)" : JSON,
  "[PolicyName](#cfn-iam-policies-policyname)" : String
}
```

### YAML<a name="aws-properties-iam-policy-syntax.yaml"></a>

```
[PolicyDocument](#cfn-iam-policies-policydocument): JSON
[PolicyName](#cfn-iam-policies-policyname): String
```

## Properties<a name="w3ab2c21c14e1308b7"></a>

`PolicyDocument`  <a name="cfn-iam-policies-policydocument"></a>
A policy document that describes what actions are allowed on which resources\.  
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PolicyName`  <a name="cfn-iam-policies-policyname"></a>
The name of the policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
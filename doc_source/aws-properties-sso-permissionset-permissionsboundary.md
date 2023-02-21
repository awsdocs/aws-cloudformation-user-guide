# AWS::SSO::PermissionSet PermissionsBoundary<a name="aws-properties-sso-permissionset-permissionsboundary"></a>

Specifies the configuration of the AWS managed or customer managed policy that you want to set as a permissions boundary\. Specify either `CustomerManagedPolicyReference` to use the name and path of a customer managed policy, or `ManagedPolicyArn` to use the ARN of an AWS managed policy\. A permissions boundary represents the maximum permissions that any policy can grant your role\. For more information, see [Permissions boundaries for IAM entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html) in the *IAM User Guide*\.

**Important**  
Policies used as permissions boundaries don't provide permissions\. You must also attach an IAM policy to the role\. To learn how the effective permissions for a role are evaluated, see [IAM JSON policy evaluation logic](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html) in the *IAM User Guide*\.

## Syntax<a name="aws-properties-sso-permissionset-permissionsboundary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sso-permissionset-permissionsboundary-syntax.json"></a>

```
{
  "[CustomerManagedPolicyReference](#cfn-sso-permissionset-permissionsboundary-customermanagedpolicyreference)" : CustomerManagedPolicyReference,
  "[ManagedPolicyArn](#cfn-sso-permissionset-permissionsboundary-managedpolicyarn)" : String
}
```

### YAML<a name="aws-properties-sso-permissionset-permissionsboundary-syntax.yaml"></a>

```
  [CustomerManagedPolicyReference](#cfn-sso-permissionset-permissionsboundary-customermanagedpolicyreference): 
    CustomerManagedPolicyReference
  [ManagedPolicyArn](#cfn-sso-permissionset-permissionsboundary-managedpolicyarn): String
```

## Properties<a name="aws-properties-sso-permissionset-permissionsboundary-properties"></a>

`CustomerManagedPolicyReference`  <a name="cfn-sso-permissionset-permissionsboundary-customermanagedpolicyreference"></a>
Specifies the name and path of a customer managed policy\. You must have an IAM policy that matches the name and path in each AWS account where you want to deploy your permission set\.  
*Required*: No  
*Type*: [CustomerManagedPolicyReference](aws-properties-sso-permissionset-customermanagedpolicyreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedPolicyArn`  <a name="cfn-sso-permissionset-permissionsboundary-managedpolicyarn"></a>
The AWS managed policy ARN that you want to attach to a permission set as a permissions boundary\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws|aws-us-gov|aws-cn|aws-iso|aws-iso-b):iam::aws:policy/[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
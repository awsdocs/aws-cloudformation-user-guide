# AWS::CloudFormation::StackSet AutoDeployment<a name="aws-properties-cloudformation-stackset-autodeployment"></a>

\[`Service-managed` permissions\] Describes whether StackSets automatically deploys to AWS Organizations accounts that are added to a target organizational unit \(OU\)\.

## Syntax<a name="aws-properties-cloudformation-stackset-autodeployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-autodeployment-syntax.json"></a>

```
{
  "[Enabled](#cfn-cloudformation-stackset-autodeployment-enabled)" : Boolean,
  "[RetainStacksOnAccountRemoval](#cfn-cloudformation-stackset-autodeployment-retainstacksonaccountremoval)" : Boolean
}
```

### YAML<a name="aws-properties-cloudformation-stackset-autodeployment-syntax.yaml"></a>

```
  [Enabled](#cfn-cloudformation-stackset-autodeployment-enabled): Boolean
  [RetainStacksOnAccountRemoval](#cfn-cloudformation-stackset-autodeployment-retainstacksonaccountremoval): Boolean
```

## Properties<a name="aws-properties-cloudformation-stackset-autodeployment-properties"></a>

`Enabled`  <a name="cfn-cloudformation-stackset-autodeployment-enabled"></a>
If set to `true`, StackSets automatically deploys additional stack instances to AWS Organizations accounts that are added to a target organization or organizational unit \(OU\) in the specified Regions\. If an account is removed from a target organization or OU, StackSets deletes stack instances from the account in the specified Regions\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetainStacksOnAccountRemoval`  <a name="cfn-cloudformation-stackset-autodeployment-retainstacksonaccountremoval"></a>
If set to `true`, stack resources are retained when an account is removed from a target organization or OU\. If set to `false`, stack resources are deleted\. Specify only if `Enabled` is set to `True`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
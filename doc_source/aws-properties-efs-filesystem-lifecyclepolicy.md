# AWS::EFS::FileSystem LifecyclePolicy<a name="aws-properties-efs-filesystem-lifecyclepolicy"></a>

Describes a policy used by EFS lifecycle management to transition files to the Infrequent Access \(IA\) storage class\. For more information, see [EFS Lifecycle Management](https://docs.aws.amazon.com/efs/latest/ug/lifecycle-management-efs.html) in the *Amazon EFS User Guide*\.

## Syntax<a name="aws-properties-efs-filesystem-lifecyclepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-filesystem-lifecyclepolicy-syntax.json"></a>

```
{
  "[TransitionToIA](#cfn-efs-filesystem-lifecyclepolicy-transitiontoia)" : String
}
```

### YAML<a name="aws-properties-efs-filesystem-lifecyclepolicy-syntax.yaml"></a>

```
  [TransitionToIA](#cfn-efs-filesystem-lifecyclepolicy-transitiontoia): String
```

## Properties<a name="aws-properties-efs-filesystem-lifecyclepolicy-properties"></a>

`TransitionToIA`  <a name="cfn-efs-filesystem-lifecyclepolicy-transitiontoia"></a>
 A value that describes the period of time that a file is not accessed, after which it transitions to the IA storage class\. Metadata operations such as listing the contents of a directory don't count as file access events\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AFTER_14_DAYS | AFTER_30_DAYS | AFTER_60_DAYS | AFTER_7_DAYS | AFTER_90_DAYS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
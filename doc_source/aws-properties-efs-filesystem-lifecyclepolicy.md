# AWS::EFS::FileSystem LifecyclePolicy<a name="aws-properties-efs-filesystem-lifecyclepolicy"></a>

Describes a policy used by EFS lifecycle management and EFS Intelligent\-Tiering that specifies when to transition files into and out of the file system's Infrequent Access \(IA\) storage class\. For more information, see [EFS Intelligent‐Tiering and EFS Lifecycle Management](https://docs.aws.amazon.com/efs/latest/ug/lifecycle-management-efs.html)\.

**Note**  
Each `LifecyclePolicy` object can have only a single transition\. This means that in a request body, `LifecyclePolicies` must be structured as an array of `LifecyclePolicy` objects, one object for each transition, `TransitionToIA`, `TransitionToPrimaryStorageClass`\.
See the AWS::EFS::FileSystem examples for the correct `LifecyclePolicy` structure\. Do not use the syntax shown on this page\.

## Syntax<a name="aws-properties-efs-filesystem-lifecyclepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-filesystem-lifecyclepolicy-syntax.json"></a>

```
{
  "[TransitionToIA](#cfn-efs-filesystem-lifecyclepolicy-transitiontoia)" : String,
  "[TransitionToPrimaryStorageClass](#cfn-efs-filesystem-lifecyclepolicy-transitiontoprimarystorageclass)" : String
}
```

### YAML<a name="aws-properties-efs-filesystem-lifecyclepolicy-syntax.yaml"></a>

```
  [TransitionToIA](#cfn-efs-filesystem-lifecyclepolicy-transitiontoia): String
  [TransitionToPrimaryStorageClass](#cfn-efs-filesystem-lifecyclepolicy-transitiontoprimarystorageclass): String
```

## Properties<a name="aws-properties-efs-filesystem-lifecyclepolicy-properties"></a>

`TransitionToIA`  <a name="cfn-efs-filesystem-lifecyclepolicy-transitiontoia"></a>
 Describes the period of time that a file is not accessed, after which it transitions to IA storage\. Metadata operations such as listing the contents of a directory don't count as file access events\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AFTER_14_DAYS | AFTER_1_DAY | AFTER_30_DAYS | AFTER_60_DAYS | AFTER_7_DAYS | AFTER_90_DAYS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitionToPrimaryStorageClass`  <a name="cfn-efs-filesystem-lifecyclepolicy-transitiontoprimarystorageclass"></a>
Describes when to transition a file from IA storage to primary storage\. Metadata operations such as listing the contents of a directory don't count as file access events\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AFTER_1_ACCESS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
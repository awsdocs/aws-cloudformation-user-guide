# AWS::DLM::LifecyclePolicy EventParameters<a name="aws-properties-dlm-lifecyclepolicy-eventparameters"></a>

Specifies an event that triggers an event\-based policy\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-eventparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-eventparameters-syntax.json"></a>

```
{
  "[DescriptionRegex](#cfn-dlm-lifecyclepolicy-eventparameters-descriptionregex)" : String,
  "[EventType](#cfn-dlm-lifecyclepolicy-eventparameters-eventtype)" : String,
  "[SnapshotOwner](#cfn-dlm-lifecyclepolicy-eventparameters-snapshotowner)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-eventparameters-syntax.yaml"></a>

```
  [DescriptionRegex](#cfn-dlm-lifecyclepolicy-eventparameters-descriptionregex): String
  [EventType](#cfn-dlm-lifecyclepolicy-eventparameters-eventtype): String
  [SnapshotOwner](#cfn-dlm-lifecyclepolicy-eventparameters-snapshotowner): 
    - String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-eventparameters-properties"></a>

`DescriptionRegex`  <a name="cfn-dlm-lifecyclepolicy-eventparameters-descriptionregex"></a>
The snapshot description that can trigger the policy\. The description pattern is specified using a regular expression\. The policy runs only if a snapshot with a description that matches the specified pattern is shared with your account\.  
For example, specifying `^.*Created for policy: policy-1234567890abcdef0.*$` configures the policy to run only if snapshots created by policy `policy-1234567890abcdef0` are shared with your account\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Pattern*: `[\p{all}]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventType`  <a name="cfn-dlm-lifecyclepolicy-eventparameters-eventtype"></a>
The type of event\. Currently, only snapshot sharing events are supported\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `shareSnapshot`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotOwner`  <a name="cfn-dlm-lifecyclepolicy-eventparameters-snapshotowner"></a>
The IDs of the AWS accounts that can trigger policy by sharing snapshots with your account\. The policy only runs if one of the specified AWS accounts shares a snapshot with your account\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
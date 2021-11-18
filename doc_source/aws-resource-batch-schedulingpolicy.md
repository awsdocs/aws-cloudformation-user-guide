# AWS::Batch::SchedulingPolicy<a name="aws-resource-batch-schedulingpolicy"></a>

The `AWS::Batch::SchedulingPolicy` resource specifies the parameters for an AWS Batch scheduling policy\. For more information, see [Scheduling Policies](https://docs.aws.amazon.com/batch/latest/userguide/scheduling_policies.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-resource-batch-schedulingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-schedulingpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::SchedulingPolicy",
  "Properties" : {
      "[FairsharePolicy](#cfn-batch-schedulingpolicy-fairsharepolicy)" : FairsharePolicy,
      "[Name](#cfn-batch-schedulingpolicy-name)" : String,
      "[Tags](#cfn-batch-schedulingpolicy-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-batch-schedulingpolicy-syntax.yaml"></a>

```
Type: AWS::Batch::SchedulingPolicy
Properties: 
  [FairsharePolicy](#cfn-batch-schedulingpolicy-fairsharepolicy): 
    FairsharePolicy
  [Name](#cfn-batch-schedulingpolicy-name): String
  [Tags](#cfn-batch-schedulingpolicy-tags): 
    Key : Value
```

## Properties<a name="aws-resource-batch-schedulingpolicy-properties"></a>

`FairsharePolicy`  <a name="cfn-batch-schedulingpolicy-fairsharepolicy"></a>
The fair share policy of the scheduling policy\.  
*Required*: No  
*Type*: [FairsharePolicy](aws-properties-batch-schedulingpolicy-fairsharepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-batch-schedulingpolicy-name"></a>
The name of the scheduling policy\. It can be up to 128 letters long\. It can contain uppercase and lowercase letters, numbers, hyphens \(\-\), and underscores \(\_\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-batch-schedulingpolicy-tags"></a>
The tags that you apply to the scheduling policy to help you categorize and organize your resources\. Each tag consists of a key and an optional value\. For more information, see [Tagging AWS Resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in * AWS General Reference*\.  
These tags can be updated or removed using the [TagResource](https://docs.aws.amazon.com/batch/latest/APIReference/API_TagResource.html) and [UntagResource](https://docs.aws.amazon.com/batch/latest/APIReference/API_UntagResource.html) API operations\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-batch-schedulingpolicy-return-values"></a>

### Ref<a name="aws-resource-batch-schedulingpolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the scheduling policy ARN, such as `arn:aws:batch:us-east-1:111122223333:scheduling-policy/HighPriority`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-batch-schedulingpolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-batch-schedulingpolicy-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the scheduling policy ARN, such as `arn:aws:batch:us-east-1:111122223333:scheduling-policy/HighPriority`\.

## See also<a name="aws-resource-batch-schedulingpolicy--seealso"></a>
+  [Scheduling Policy Parameters](https://docs.aws.amazon.com/batch/latest/userguide/scheduling_policy_parameters.html) in the *AWS Batch User Guide*\.
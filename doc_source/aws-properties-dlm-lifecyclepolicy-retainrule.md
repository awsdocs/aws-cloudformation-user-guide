# AWS::DLM::LifecyclePolicy RetainRule<a name="aws-properties-dlm-lifecyclepolicy-retainrule"></a>

Specifies the retention rule for a lifecycle policy\. You can retain snapshots based on either a count or a time interval\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-retainrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-retainrule-syntax.json"></a>

```
{
  "[Count](#cfn-dlm-lifecyclepolicy-retainrule-count)" : Integer,
  "[Interval](#cfn-dlm-lifecyclepolicy-retainrule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-retainrule-intervalunit)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-retainrule-syntax.yaml"></a>

```
  [Count](#cfn-dlm-lifecyclepolicy-retainrule-count): Integer
  [Interval](#cfn-dlm-lifecyclepolicy-retainrule-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-retainrule-intervalunit): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-retainrule-properties"></a>

`Count`  <a name="cfn-dlm-lifecyclepolicy-retainrule-count"></a>
The number of snapshots to retain for each volume, up to a maximum of 1000\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-dlm-lifecyclepolicy-retainrule-interval"></a>
The amount of time to retain each snapshot\. The maximum is 100 years\. This is equivalent to 1200 months, 5200 weeks, or 36500 days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-retainrule-intervalunit"></a>
The unit of time for time\-based retention\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAYS | MONTHS | WEEKS | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
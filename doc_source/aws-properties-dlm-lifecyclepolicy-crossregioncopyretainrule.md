# AWS::DLM::LifecyclePolicy CrossRegionCopyRetainRule<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule"></a>

Specifies the retention rule for cross\-Region snapshot copies\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule-syntax.json"></a>

```
{
  "[Interval](#cfn-dlm-lifecyclepolicy-crossregioncopyretainrule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-crossregioncopyretainrule-intervalunit)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule-syntax.yaml"></a>

```
  [Interval](#cfn-dlm-lifecyclepolicy-crossregioncopyretainrule-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-crossregioncopyretainrule-intervalunit): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule-properties"></a>

`Interval`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyretainrule-interval"></a>
The amount of time to retain each snapshot\. The maximum is 100 years\. This is equivalent to 1200 months, 5200 weeks, or 36500 days\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyretainrule-intervalunit"></a>
The unit of time for time\-based retention\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAYS | MONTHS | WEEKS | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
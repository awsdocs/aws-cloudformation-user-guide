# AWS::DLM::LifecyclePolicy FastRestoreRule<a name="aws-properties-dlm-lifecyclepolicy-fastrestorerule"></a>

Specifies a rule for enabling fast snapshot restore\. You can enable fast snapshot restore based on either a count or a time interval\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-fastrestorerule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-fastrestorerule-syntax.json"></a>

```
{
  "[AvailabilityZones](#cfn-dlm-lifecyclepolicy-fastrestorerule-availabilityzones)" : [ String, ... ],
  "[Count](#cfn-dlm-lifecyclepolicy-fastrestorerule-count)" : Integer,
  "[Interval](#cfn-dlm-lifecyclepolicy-fastrestorerule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-fastrestorerule-intervalunit)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-fastrestorerule-syntax.yaml"></a>

```
  [AvailabilityZones](#cfn-dlm-lifecyclepolicy-fastrestorerule-availabilityzones): 
    - String
  [Count](#cfn-dlm-lifecyclepolicy-fastrestorerule-count): Integer
  [Interval](#cfn-dlm-lifecyclepolicy-fastrestorerule-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-fastrestorerule-intervalunit): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-fastrestorerule-properties"></a>

`AvailabilityZones`  <a name="cfn-dlm-lifecyclepolicy-fastrestorerule-availabilityzones"></a>
The Availability Zones in which to enable fast snapshot restore\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Count`  <a name="cfn-dlm-lifecyclepolicy-fastrestorerule-count"></a>
The number of snapshots to be enabled with fast snapshot restore\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-dlm-lifecyclepolicy-fastrestorerule-interval"></a>
The amount of time to enable fast snapshot restore\. The maximum is 100 years\. This is equivalent to 1200 months, 5200 weeks, or 36500 days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-fastrestorerule-intervalunit"></a>
The unit of time for enabling fast snapshot restore\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAYS | MONTHS | WEEKS | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
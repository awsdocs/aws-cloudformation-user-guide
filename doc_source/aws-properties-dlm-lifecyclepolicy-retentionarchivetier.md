# AWS::DLM::LifecyclePolicy RetentionArchiveTier<a name="aws-properties-dlm-lifecyclepolicy-retentionarchivetier"></a>

 **\[Snapshot policies only\]** Describes the retention rule for archived snapshots\. Once the archive retention threshold is met, the snapshots are permanently deleted from the archive tier\.

**Note**  
The archive retention rule must retain snapshots in the archive tier for a minimum of 90 days\.

For **count\-based schedules**, you must specify **Count**\. For **age\-based schedules**, you must specify **Interval** and ** IntervalUnit**\.

For more information about using snapshot archiving, see [Considerations for snapshot lifecycle policies](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-ami-policy.html#dlm-archive)\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-retentionarchivetier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-retentionarchivetier-syntax.json"></a>

```
{
  "[Count](#cfn-dlm-lifecyclepolicy-retentionarchivetier-count)" : Integer,
  "[Interval](#cfn-dlm-lifecyclepolicy-retentionarchivetier-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-retentionarchivetier-intervalunit)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-retentionarchivetier-syntax.yaml"></a>

```
  [Count](#cfn-dlm-lifecyclepolicy-retentionarchivetier-count): Integer
  [Interval](#cfn-dlm-lifecyclepolicy-retentionarchivetier-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-retentionarchivetier-intervalunit): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-retentionarchivetier-properties"></a>

`Count`  <a name="cfn-dlm-lifecyclepolicy-retentionarchivetier-count"></a>
The maximum number of snapshots to retain in the archive storage tier for each volume\. The count must ensure that each snapshot remains in the archive tier for at least 90 days\. For example, if the schedule creates snapshots every 30 days, you must specify a count of 3 or more to ensure that each snapshot is archived for at least 90 days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-dlm-lifecyclepolicy-retentionarchivetier-interval"></a>
Specifies the period of time to retain snapshots in the archive tier\. After this period expires, the snapshot is permanently deleted\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-retentionarchivetier-intervalunit"></a>
The unit of time in which to measure the **Interval**\. For example, to retain a snapshots in the archive tier for 6 months, specify `Interval=6` and `IntervalUnit=MONTHS`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAYS | MONTHS | WEEKS | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
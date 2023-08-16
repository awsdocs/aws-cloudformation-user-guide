# AWS::FSx::Volume SnaplockRetentionPeriod<a name="aws-properties-fsx-volume-snaplockretentionperiod"></a>

The configuration to set the retention period of an FSx for ONTAP SnapLock volume\. The retention period includes default, maximum, and minimum settings\. For more information, see [Working with the retention period in SnapLock](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/snaplock-retention.html)\. 

## Syntax<a name="aws-properties-fsx-volume-snaplockretentionperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-snaplockretentionperiod-syntax.json"></a>

```
{
  "[DefaultRetention](#cfn-fsx-volume-snaplockretentionperiod-defaultretention)" : RetentionPeriod,
  "[MaximumRetention](#cfn-fsx-volume-snaplockretentionperiod-maximumretention)" : RetentionPeriod,
  "[MinimumRetention](#cfn-fsx-volume-snaplockretentionperiod-minimumretention)" : RetentionPeriod
}
```

### YAML<a name="aws-properties-fsx-volume-snaplockretentionperiod-syntax.yaml"></a>

```
  [DefaultRetention](#cfn-fsx-volume-snaplockretentionperiod-defaultretention): 
    RetentionPeriod
  [MaximumRetention](#cfn-fsx-volume-snaplockretentionperiod-maximumretention): 
    RetentionPeriod
  [MinimumRetention](#cfn-fsx-volume-snaplockretentionperiod-minimumretention): 
    RetentionPeriod
```

## Properties<a name="aws-properties-fsx-volume-snaplockretentionperiod-properties"></a>

`DefaultRetention`  <a name="cfn-fsx-volume-snaplockretentionperiod-defaultretention"></a>
The retention period assigned to a write once, read many \(WORM\) file by default if an explicit retention period is not set for an FSx for ONTAP SnapLock volume\. The default retention period must be greater than or equal to the minimum retention period and less than or equal to the maximum retention period\.   
*Required*: Yes  
*Type*: [RetentionPeriod](aws-properties-fsx-volume-retentionperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumRetention`  <a name="cfn-fsx-volume-snaplockretentionperiod-maximumretention"></a>
The longest retention period that can be assigned to a WORM file on an FSx for ONTAP SnapLock volume\.   
*Required*: Yes  
*Type*: [RetentionPeriod](aws-properties-fsx-volume-retentionperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumRetention`  <a name="cfn-fsx-volume-snaplockretentionperiod-minimumretention"></a>
The shortest retention period that can be assigned to a WORM file on an FSx for ONTAP SnapLock volume\.   
*Required*: Yes  
*Type*: [RetentionPeriod](aws-properties-fsx-volume-retentionperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
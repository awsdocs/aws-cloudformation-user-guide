# AWS::FSx::Volume RetentionPeriod<a name="aws-properties-fsx-volume-retentionperiod"></a>

Specifies the retention period of an FSx for ONTAP SnapLock volume\. After it is set, it can't be changed\. Files can't be deleted or modified during the retention period\. 

For more information, see [Working with the retention period in SnapLock](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/snaplock-retention.html)\. 

## Syntax<a name="aws-properties-fsx-volume-retentionperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-retentionperiod-syntax.json"></a>

```
{
  "[Type](#cfn-fsx-volume-retentionperiod-type)" : String,
  "[Value](#cfn-fsx-volume-retentionperiod-value)" : Integer
}
```

### YAML<a name="aws-properties-fsx-volume-retentionperiod-syntax.yaml"></a>

```
  [Type](#cfn-fsx-volume-retentionperiod-type): String
  [Value](#cfn-fsx-volume-retentionperiod-value): Integer
```

## Properties<a name="aws-properties-fsx-volume-retentionperiod-properties"></a>

`Type`  <a name="cfn-fsx-volume-retentionperiod-type"></a>
Defines the type of time for the retention period of an FSx for ONTAP SnapLock volume\. Set it to one of the valid types\. If you set it to `INFINITE`, the files are retained forever\. If you set it to `UNSPECIFIED`, the files are retained until you set an explicit retention period\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAYS | HOURS | INFINITE | MINUTES | MONTHS | SECONDS | UNSPECIFIED | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-fsx-volume-retentionperiod-value"></a>
Defines the amount of time for the retention period of an FSx for ONTAP SnapLock volume\. You can't set a value for `INFINITE` or `UNSPECIFIED`\. For all other options, the following ranges are valid:   
+  `Seconds`: 0 \- 65,535
+  `Minutes`: 0 \- 65,535
+  `Hours`: 0 \- 24
+  `Days`: 0 \- 365
+  `Months`: 0 \- 12
+  `Years`: 0 \- 100
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
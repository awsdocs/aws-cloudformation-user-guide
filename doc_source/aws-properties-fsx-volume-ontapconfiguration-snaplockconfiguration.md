# AWS::FSx::Volume SnaplockConfiguration<a name="aws-properties-fsx-volume-ontapconfiguration-snaplockconfiguration"></a>

Specifies the SnapLock configuration for an FSx for ONTAP SnapLock volume\. 

## Syntax<a name="aws-properties-fsx-volume-ontapconfiguration-snaplockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-ontapconfiguration-snaplockconfiguration-syntax.json"></a>

```
{
  "[AuditLogVolume](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-auditlogvolume)" : String,
  "[AutocommitPeriod](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-autocommitperiod)" : AutocommitPeriod,
  "[PrivilegedDelete](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-privilegeddelete)" : String,
  "[RetentionPeriod](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-retentionperiod)" : SnaplockRetentionPeriod,
  "[SnaplockType](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-snaplocktype)" : String,
  "[VolumeAppendModeEnabled](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-volumeappendmodeenabled)" : String
}
```

### YAML<a name="aws-properties-fsx-volume-ontapconfiguration-snaplockconfiguration-syntax.yaml"></a>

```
  [AuditLogVolume](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-auditlogvolume): String
  [AutocommitPeriod](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-autocommitperiod): 
    AutocommitPeriod
  [PrivilegedDelete](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-privilegeddelete): String
  [RetentionPeriod](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-retentionperiod): 
    SnaplockRetentionPeriod
  [SnaplockType](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-snaplocktype): String
  [VolumeAppendModeEnabled](#cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-volumeappendmodeenabled): String
```

## Properties<a name="aws-properties-fsx-volume-ontapconfiguration-snaplockconfiguration-properties"></a>

`AuditLogVolume`  <a name="cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-auditlogvolume"></a>
Enables or disables the audit log volume for an FSx for ONTAP SnapLock volume\. The default value is `false`\. If you set `AuditLogVolume` to `true`, the SnapLock volume is created as an audit log volume\. The minimum retention period for an audit log volume is six months\.   
For more information, see [ SnapLock audit log volumes](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/how-snaplock-works.html#snaplock-audit-log-volume)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutocommitPeriod`  <a name="cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-autocommitperiod"></a>
The configuration object for setting the autocommit period of files in an FSx for ONTAP SnapLock volume\.   
*Required*: No  
*Type*: [AutocommitPeriod](aws-properties-fsx-volume-ontapconfiguration-snaplockconfiguration-autocommitperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivilegedDelete`  <a name="cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-privilegeddelete"></a>
Enables, disables, or permanently disables privileged delete on an FSx for ONTAP SnapLock Enterprise volume\. Enabling privileged delete allows SnapLock administrators to delete write once, read many \(WORM\) files even if they have active retention periods\. `PERMANENTLY_DISABLED` is a terminal state\. If privileged delete is permanently disabled on a SnapLock volume, you can't re\-enable it\. The default value is `DISABLED`\.   
For more information, see [Privileged delete](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/snaplock-enterprise.html#privileged-delete)\.   
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED | PERMANENTLY_DISABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetentionPeriod`  <a name="cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-retentionperiod"></a>
Specifies the retention period of an FSx for ONTAP SnapLock volume\.   
*Required*: No  
*Type*: [SnaplockRetentionPeriod](aws-properties-fsx-volume-snaplockretentionperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnaplockType`  <a name="cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-snaplocktype"></a>
Specifies the retention mode of an FSx for ONTAP SnapLock volume\. After it is set, it can't be changed\. You can choose one of the following retention modes:   
+  `COMPLIANCE`: Files transitioned to write once, read many \(WORM\) on a Compliance volume can't be deleted until their retention periods expire\. This retention mode is used to address government or industry\-specific mandates or to protect against ransomware attacks\. For more information, see [SnapLock Compliance](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/snaplock-compliance.html)\. 
+  `ENTERPRISE`: Files transitioned to WORM on an Enterprise volume can be deleted by authorized users before their retention periods expire using privileged delete\. This retention mode is used to advance an organization's data integrity and internal compliance or to test retention settings before using SnapLock Compliance\. For more information, see [SnapLock Enterprise](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/snaplock-enterprise.html)\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `COMPLIANCE | ENTERPRISE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeAppendModeEnabled`  <a name="cfn-fsx-volume-ontapconfiguration-snaplockconfiguration-volumeappendmodeenabled"></a>
Enables or disables volume\-append mode on an FSx for ONTAP SnapLock volume\. Volume\-append mode allows you to create WORM\-appendable files and write data to them incrementally\. The default value is `false`\.   
For more information, see [Volume\-append mode](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/worm-state.html#worm-state-append)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
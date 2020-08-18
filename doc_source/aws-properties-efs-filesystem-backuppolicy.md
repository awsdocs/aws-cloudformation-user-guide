# AWS::EFS::FileSystem BackupPolicy<a name="aws-properties-efs-filesystem-backuppolicy"></a>

The backup policy turns automatic backups for the file system on or off\.

## Syntax<a name="aws-properties-efs-filesystem-backuppolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-filesystem-backuppolicy-syntax.json"></a>

```
{
  "[Status](#cfn-efs-filesystem-backuppolicy-status)" : String
}
```

### YAML<a name="aws-properties-efs-filesystem-backuppolicy-syntax.yaml"></a>

```
  [Status](#cfn-efs-filesystem-backuppolicy-status): String
```

## Properties<a name="aws-properties-efs-filesystem-backuppolicy-properties"></a>

`Status`  <a name="cfn-efs-filesystem-backuppolicy-status"></a>
Set the backup policy status for the file system\.  
+  ** `ENABLED`** \- Turns automatic backups on for the file system\. 
+  ** `DISABLED`** \- Turns automatic backups off for the file system\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | DISABLING | ENABLED | ENABLING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
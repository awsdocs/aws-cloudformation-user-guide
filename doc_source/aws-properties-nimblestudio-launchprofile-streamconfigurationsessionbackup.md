# AWS::NimbleStudio::LaunchProfile StreamConfigurationSessionBackup<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionbackup"></a>

Configures how streaming sessions are backed up when launched from this launch profile\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionbackup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionbackup-syntax.json"></a>

```
{
  "[MaxBackupsToRetain](#cfn-nimblestudio-launchprofile-streamconfigurationsessionbackup-maxbackupstoretain)" : Double,
  "[Mode](#cfn-nimblestudio-launchprofile-streamconfigurationsessionbackup-mode)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionbackup-syntax.yaml"></a>

```
  [MaxBackupsToRetain](#cfn-nimblestudio-launchprofile-streamconfigurationsessionbackup-maxbackupstoretain): Double
  [Mode](#cfn-nimblestudio-launchprofile-streamconfigurationsessionbackup-mode): String
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionbackup-properties"></a>

`MaxBackupsToRetain`  <a name="cfn-nimblestudio-launchprofile-streamconfigurationsessionbackup-maxbackupstoretain"></a>
The maximum number of backups that each streaming session created from this launch profile can have\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-nimblestudio-launchprofile-streamconfigurationsessionbackup-mode"></a>
Specifies how artists sessions are backed up\.  
Configures backups for streaming sessions launched with this launch profile\. The default value is `DEACTIVATED`, which means that backups are deactivated\. To allow backups, set this value to `AUTOMATIC`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MediaLive::Channel ArchiveGroupSettings<a name="aws-properties-medialive-channel-archivegroupsettings"></a>

The settings for an archive output group\.

The parent of this entity is OutputGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-archivegroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-archivegroupsettings-syntax.json"></a>

```
{
  "[Destination](#cfn-medialive-channel-archivegroupsettings-destination)" : OutputLocationRef,
  "[RolloverInterval](#cfn-medialive-channel-archivegroupsettings-rolloverinterval)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-archivegroupsettings-syntax.yaml"></a>

```
  [Destination](#cfn-medialive-channel-archivegroupsettings-destination): 
    OutputLocationRef
  [RolloverInterval](#cfn-medialive-channel-archivegroupsettings-rolloverinterval): Integer
```

## Properties<a name="aws-properties-medialive-channel-archivegroupsettings-properties"></a>

`Destination`  <a name="cfn-medialive-channel-archivegroupsettings-destination"></a>
A directory and base file name where archive files should be written\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RolloverInterval`  <a name="cfn-medialive-channel-archivegroupsettings-rolloverinterval"></a>
The number of seconds to write to an archive file before closing and starting a new one\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MediaLive::Channel ArchiveOutputSettings<a name="aws-properties-medialive-channel-archiveoutputsettings"></a>

The archive output settings\.

The parent of this entity is OutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-archiveoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-archiveoutputsettings-syntax.json"></a>

```
{
  "[ContainerSettings](#cfn-medialive-channel-archiveoutputsettings-containersettings)" : ArchiveContainerSettings,
  "[Extension](#cfn-medialive-channel-archiveoutputsettings-extension)" : String,
  "[NameModifier](#cfn-medialive-channel-archiveoutputsettings-namemodifier)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-archiveoutputsettings-syntax.yaml"></a>

```
  [ContainerSettings](#cfn-medialive-channel-archiveoutputsettings-containersettings): 
    ArchiveContainerSettings
  [Extension](#cfn-medialive-channel-archiveoutputsettings-extension): String
  [NameModifier](#cfn-medialive-channel-archiveoutputsettings-namemodifier): String
```

## Properties<a name="aws-properties-medialive-channel-archiveoutputsettings-properties"></a>

`ContainerSettings`  <a name="cfn-medialive-channel-archiveoutputsettings-containersettings"></a>
The settings that are specific to the container type of the file\.  
*Required*: No  
*Type*: [ArchiveContainerSettings](aws-properties-medialive-channel-archivecontainersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Extension`  <a name="cfn-medialive-channel-archiveoutputsettings-extension"></a>
The output file extension\. If excluded, this is auto\-selected from the container type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NameModifier`  <a name="cfn-medialive-channel-archiveoutputsettings-namemodifier"></a>
A string that is concatenated to the end of the destination file name\. The string is required for multiple outputs of the same type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
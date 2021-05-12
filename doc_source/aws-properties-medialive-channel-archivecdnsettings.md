# AWS::MediaLive::Channel ArchiveCdnSettings<a name="aws-properties-medialive-channel-archivecdnsettings"></a>

Settings to configure the destination of an Archive output\.

The parent of this entity is ArchiveGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-archivecdnsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-archivecdnsettings-syntax.json"></a>

```
{
  "[ArchiveS3Settings](#cfn-medialive-channel-archivecdnsettings-archives3settings)" : ArchiveS3Settings
}
```

### YAML<a name="aws-properties-medialive-channel-archivecdnsettings-syntax.yaml"></a>

```
  [ArchiveS3Settings](#cfn-medialive-channel-archivecdnsettings-archives3settings): 
    ArchiveS3Settings
```

## Properties<a name="aws-properties-medialive-channel-archivecdnsettings-properties"></a>

`ArchiveS3Settings`  <a name="cfn-medialive-channel-archivecdnsettings-archives3settings"></a>
Sets up Amazon S3 as the destination for this Archive output\.  
*Required*: No  
*Type*: [ArchiveS3Settings](aws-properties-medialive-channel-archives3settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
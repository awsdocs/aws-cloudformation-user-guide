# AWS::NimbleStudio::StudioComponent SharedFileSystemConfiguration<a name="aws-properties-nimblestudio-studiocomponent-sharedfilesystemconfiguration"></a>

The configuration for a shared file storage system that is associated with a studio resource\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-sharedfilesystemconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-sharedfilesystemconfiguration-syntax.json"></a>

```
{
  "[Endpoint](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-endpoint)" : String,
  "[FileSystemId](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-filesystemid)" : String,
  "[LinuxMountPoint](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-linuxmountpoint)" : String,
  "[ShareName](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-sharename)" : String,
  "[WindowsMountDrive](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-windowsmountdrive)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-sharedfilesystemconfiguration-syntax.yaml"></a>

```
  [Endpoint](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-endpoint): String
  [FileSystemId](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-filesystemid): String
  [LinuxMountPoint](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-linuxmountpoint): String
  [ShareName](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-sharename): String
  [WindowsMountDrive](#cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-windowsmountdrive): String
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-sharedfilesystemconfiguration-properties"></a>

`Endpoint`  <a name="cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-endpoint"></a>
The endpoint of the shared file system that is accessed by the studio component resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileSystemId`  <a name="cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-filesystemid"></a>
The unique identifier for a file system\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LinuxMountPoint`  <a name="cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-linuxmountpoint"></a>
The mount location for a shared file system on a Linux virtual workstation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShareName`  <a name="cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-sharename"></a>
The name of the file share\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowsMountDrive`  <a name="cfn-nimblestudio-studiocomponent-sharedfilesystemconfiguration-windowsmountdrive"></a>
The mount location for a shared file system on a Windows virtual workstation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
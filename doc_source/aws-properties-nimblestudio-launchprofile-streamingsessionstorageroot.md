# AWS::NimbleStudio::LaunchProfile StreamingSessionStorageRoot<a name="aws-properties-nimblestudio-launchprofile-streamingsessionstorageroot"></a>

The upload storage root location \(folder\) on streaming workstations where files are uploaded\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streamingsessionstorageroot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streamingsessionstorageroot-syntax.json"></a>

```
{
  "[Linux](#cfn-nimblestudio-launchprofile-streamingsessionstorageroot-linux)" : String,
  "[Windows](#cfn-nimblestudio-launchprofile-streamingsessionstorageroot-windows)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streamingsessionstorageroot-syntax.yaml"></a>

```
  [Linux](#cfn-nimblestudio-launchprofile-streamingsessionstorageroot-linux): String
  [Windows](#cfn-nimblestudio-launchprofile-streamingsessionstorageroot-windows): String
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-streamingsessionstorageroot-properties"></a>

`Linux`  <a name="cfn-nimblestudio-launchprofile-streamingsessionstorageroot-linux"></a>
The folder path in Linux workstations where files are uploaded\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Windows`  <a name="cfn-nimblestudio-launchprofile-streamingsessionstorageroot-windows"></a>
The folder path in Windows workstations where files are uploaded\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::NimbleStudio::LaunchProfile StreamConfigurationSessionStorage<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage"></a>

The configuration for a streaming session’s upload storage\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage-syntax.json"></a>

```
{
  "[Mode](#cfn-nimblestudio-launchprofile-streamconfigurationsessionstorage-mode)" : [ String, ... ],
  "[Root](#cfn-nimblestudio-launchprofile-streamconfigurationsessionstorage-root)" : StreamingSessionStorageRoot
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage-syntax.yaml"></a>

```
  [Mode](#cfn-nimblestudio-launchprofile-streamconfigurationsessionstorage-mode): 
    - String
  [Root](#cfn-nimblestudio-launchprofile-streamconfigurationsessionstorage-root): 
    StreamingSessionStorageRoot
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage-properties"></a>

`Mode`  <a name="cfn-nimblestudio-launchprofile-streamconfigurationsessionstorage-mode"></a>
Allows artists to upload files to their workstations\. The only valid option is `UPLOAD`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Root`  <a name="cfn-nimblestudio-launchprofile-streamconfigurationsessionstorage-root"></a>
The configuration for the upload storage root of the streaming session\.  
*Required*: No  
*Type*: [StreamingSessionStorageRoot](aws-properties-nimblestudio-launchprofile-streamingsessionstorageroot.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
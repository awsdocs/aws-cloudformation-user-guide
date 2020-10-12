# AWS::MediaLive::Channel VideoSelectorSettings<a name="aws-properties-medialive-channel-videoselectorsettings"></a>

Video Selector Settings

## Syntax<a name="aws-properties-medialive-channel-videoselectorsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videoselectorsettings-syntax.json"></a>

```
{
  "[VideoSelectorPid](#cfn-medialive-channel-videoselectorsettings-videoselectorpid)" : VideoSelectorPid,
  "[VideoSelectorProgramId](#cfn-medialive-channel-videoselectorsettings-videoselectorprogramid)" : VideoSelectorProgramId
}
```

### YAML<a name="aws-properties-medialive-channel-videoselectorsettings-syntax.yaml"></a>

```
  [VideoSelectorPid](#cfn-medialive-channel-videoselectorsettings-videoselectorpid): 
    VideoSelectorPid
  [VideoSelectorProgramId](#cfn-medialive-channel-videoselectorsettings-videoselectorprogramid): 
    VideoSelectorProgramId
```

## Properties<a name="aws-properties-medialive-channel-videoselectorsettings-properties"></a>

`VideoSelectorPid`  <a name="cfn-medialive-channel-videoselectorsettings-videoselectorpid"></a>
Include this 'video selection' element if you want to use the PID to extract the video from the input\.  
*Required*: No  
*Type*: [VideoSelectorPid](aws-properties-medialive-channel-videoselectorpid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoSelectorProgramId`  <a name="cfn-medialive-channel-videoselectorsettings-videoselectorprogramid"></a>
Include this 'video selection' element if you want to use the program ID to extract the video from the input\.  
*Required*: No  
*Type*: [VideoSelectorProgramId](aws-properties-medialive-channel-videoselectorprogramid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MediaLive::Channel VideoSelectorPid<a name="aws-properties-medialive-channel-videoselectorpid"></a>

Selects a specific PID from within a video source\.

The parent of this entity is VideoSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-videoselectorpid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videoselectorpid-syntax.json"></a>

```
{
  "[Pid](#cfn-medialive-channel-videoselectorpid-pid)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-videoselectorpid-syntax.yaml"></a>

```
  [Pid](#cfn-medialive-channel-videoselectorpid-pid): Integer
```

## Properties<a name="aws-properties-medialive-channel-videoselectorpid-properties"></a>

`Pid`  <a name="cfn-medialive-channel-videoselectorpid-pid"></a>
Selects a specific PID from within a video source\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
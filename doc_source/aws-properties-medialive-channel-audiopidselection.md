# AWS::MediaLive::Channel AudioPidSelection<a name="aws-properties-medialive-channel-audiopidselection"></a>

This element specifies the audio by its PID\. This element belongs to AudioSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-audiopidselection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiopidselection-syntax.json"></a>

```
{
  "[Pid](#cfn-medialive-channel-audiopidselection-pid)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-audiopidselection-syntax.yaml"></a>

```
  [Pid](#cfn-medialive-channel-audiopidselection-pid): Integer
```

## Properties<a name="aws-properties-medialive-channel-audiopidselection-properties"></a>

`Pid`  <a name="cfn-medialive-channel-audiopidselection-pid"></a>
Selects a specific PID from within a source\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
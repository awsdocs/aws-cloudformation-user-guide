# AWS::MediaLive::Channel AudioPidSelection<a name="aws-properties-medialive-channel-audiopidselection"></a>

Used to extract audio by The PID\.

The parent of this entity is AudioSelectorSettings\.

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
Select the audio by this PID\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
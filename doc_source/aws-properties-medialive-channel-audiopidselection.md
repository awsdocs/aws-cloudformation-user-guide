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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `sa-east-1`
- `us-east-1`
- `us-west-2`

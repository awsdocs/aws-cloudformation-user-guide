# AWS::MediaLive::Channel VideoSelectorProgramId<a name="aws-properties-medialive-channel-videoselectorprogramid"></a>

Video Selector Program Id

## Syntax<a name="aws-properties-medialive-channel-videoselectorprogramid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videoselectorprogramid-syntax.json"></a>

```
{
  "[ProgramId](#cfn-medialive-channel-videoselectorprogramid-programid)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-videoselectorprogramid-syntax.yaml"></a>

```
  [ProgramId](#cfn-medialive-channel-videoselectorprogramid-programid): Integer
```

## Properties<a name="aws-properties-medialive-channel-videoselectorprogramid-properties"></a>

`ProgramId`  <a name="cfn-medialive-channel-videoselectorprogramid-programid"></a>
Selects a specific program from within a multi\-program transport stream\. If the program doesn't exist, the first program within the transport stream will be selected by default\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
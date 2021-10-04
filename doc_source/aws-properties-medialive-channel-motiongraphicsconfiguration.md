# AWS::MediaLive::Channel MotionGraphicsConfiguration<a name="aws-properties-medialive-channel-motiongraphicsconfiguration"></a>

Settings to enable and configure the motion graphics overlay feature in the channel\.

The parent of this entity is EncoderSettings\.

## Syntax<a name="aws-properties-medialive-channel-motiongraphicsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-motiongraphicsconfiguration-syntax.json"></a>

```
{
  "[MotionGraphicsInsertion](#cfn-medialive-channel-motiongraphicsconfiguration-motiongraphicsinsertion)" : String,
  "[MotionGraphicsSettings](#cfn-medialive-channel-motiongraphicsconfiguration-motiongraphicssettings)" : MotionGraphicsSettings
}
```

### YAML<a name="aws-properties-medialive-channel-motiongraphicsconfiguration-syntax.yaml"></a>

```
  [MotionGraphicsInsertion](#cfn-medialive-channel-motiongraphicsconfiguration-motiongraphicsinsertion): String
  [MotionGraphicsSettings](#cfn-medialive-channel-motiongraphicsconfiguration-motiongraphicssettings): 
    MotionGraphicsSettings
```

## Properties<a name="aws-properties-medialive-channel-motiongraphicsconfiguration-properties"></a>

`MotionGraphicsInsertion`  <a name="cfn-medialive-channel-motiongraphicsconfiguration-motiongraphicsinsertion"></a>
Enables or disables the motion graphics overlay feature in the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MotionGraphicsSettings`  <a name="cfn-medialive-channel-motiongraphicsconfiguration-motiongraphicssettings"></a>
Settings to enable and configure the motion graphics overlay feature in the channel\.  
*Required*: No  
*Type*: [MotionGraphicsSettings](aws-properties-medialive-channel-motiongraphicssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
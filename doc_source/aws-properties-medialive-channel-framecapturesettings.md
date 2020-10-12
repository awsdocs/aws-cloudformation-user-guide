# AWS::MediaLive::Channel FrameCaptureSettings<a name="aws-properties-medialive-channel-framecapturesettings"></a>

Configures the output video encode as a set of frame capatures \(JPEG files\)\. This element belongs to VideoCodecSettings\.

## Syntax<a name="aws-properties-medialive-channel-framecapturesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-framecapturesettings-syntax.json"></a>

```
{
  "[CaptureInterval](#cfn-medialive-channel-framecapturesettings-captureinterval)" : Integer,
  "[CaptureIntervalUnits](#cfn-medialive-channel-framecapturesettings-captureintervalunits)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-framecapturesettings-syntax.yaml"></a>

```
  [CaptureInterval](#cfn-medialive-channel-framecapturesettings-captureinterval): Integer
  [CaptureIntervalUnits](#cfn-medialive-channel-framecapturesettings-captureintervalunits): String
```

## Properties<a name="aws-properties-medialive-channel-framecapturesettings-properties"></a>

`CaptureInterval`  <a name="cfn-medialive-channel-framecapturesettings-captureinterval"></a>
The frequency at which to capture frames for inclusion in the output\. May be specified in either seconds or milliseconds, as specified by captureIntervalUnits\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptureIntervalUnits`  <a name="cfn-medialive-channel-framecapturesettings-captureintervalunits"></a>
Unit for the frame capture interval\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
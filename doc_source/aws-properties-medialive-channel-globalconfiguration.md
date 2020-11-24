# AWS::MediaLive::Channel GlobalConfiguration<a name="aws-properties-medialive-channel-globalconfiguration"></a>

Global Configuration

## Syntax<a name="aws-properties-medialive-channel-globalconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-globalconfiguration-syntax.json"></a>

```
{
  "[InitialAudioGain](#cfn-medialive-channel-globalconfiguration-initialaudiogain)" : Integer,
  "[InputEndAction](#cfn-medialive-channel-globalconfiguration-inputendaction)" : String,
  "[InputLossBehavior](#cfn-medialive-channel-globalconfiguration-inputlossbehavior)" : InputLossBehavior,
  "[OutputLockingMode](#cfn-medialive-channel-globalconfiguration-outputlockingmode)" : String,
  "[OutputTimingSource](#cfn-medialive-channel-globalconfiguration-outputtimingsource)" : String,
  "[SupportLowFramerateInputs](#cfn-medialive-channel-globalconfiguration-supportlowframerateinputs)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-globalconfiguration-syntax.yaml"></a>

```
  [InitialAudioGain](#cfn-medialive-channel-globalconfiguration-initialaudiogain): Integer
  [InputEndAction](#cfn-medialive-channel-globalconfiguration-inputendaction): String
  [InputLossBehavior](#cfn-medialive-channel-globalconfiguration-inputlossbehavior): 
    InputLossBehavior
  [OutputLockingMode](#cfn-medialive-channel-globalconfiguration-outputlockingmode): String
  [OutputTimingSource](#cfn-medialive-channel-globalconfiguration-outputtimingsource): String
  [SupportLowFramerateInputs](#cfn-medialive-channel-globalconfiguration-supportlowframerateinputs): String
```

## Properties<a name="aws-properties-medialive-channel-globalconfiguration-properties"></a>

`InitialAudioGain`  <a name="cfn-medialive-channel-globalconfiguration-initialaudiogain"></a>
Value to set the initial audio gain\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputEndAction`  <a name="cfn-medialive-channel-globalconfiguration-inputendaction"></a>
Indicates the action to take when the current input completes \(e\.g\. end\-of\-file\)\. When switchAndLoopInputs is configured the encoder will restart at the beginning of the first input\. When "none" is configured the encoder will transcode either black, a solid color, or a user specified slate images per the "Input Loss Behavior" configuration until the next input switch occurs \(which is controlled through the Channel Schedule API\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossBehavior`  <a name="cfn-medialive-channel-globalconfiguration-inputlossbehavior"></a>
Settings for system actions when input is lost\.  
*Required*: No  
*Type*: [InputLossBehavior](aws-properties-medialive-channel-inputlossbehavior.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputLockingMode`  <a name="cfn-medialive-channel-globalconfiguration-outputlockingmode"></a>
Indicates how MediaLive pipelines are synchronized\. PIPELINE\_LOCKING \- MediaLive will attempt to synchronize the output of each pipeline to the other\. EPOCH\_LOCKING \- MediaLive will attempt to synchronize the output of each pipeline to the Unix epoch\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputTimingSource`  <a name="cfn-medialive-channel-globalconfiguration-outputtimingsource"></a>
Indicates whether the rate of frames emitted by the Live encoder should be paced by its system clock \(which optionally may be locked to another source via NTP\) or should be locked to the clock of the source that is providing the input stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportLowFramerateInputs`  <a name="cfn-medialive-channel-globalconfiguration-supportlowframerateinputs"></a>
Adjusts video input buffer for streams with very low video framerates\. This is commonly set to enabled for music channels with less than one video frame per second\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
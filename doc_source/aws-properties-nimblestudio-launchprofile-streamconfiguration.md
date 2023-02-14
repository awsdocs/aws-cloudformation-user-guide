# AWS::NimbleStudio::LaunchProfile StreamConfiguration<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration"></a>

A configuration for a streaming session\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax.json"></a>

```
{
  "[ClipboardMode](#cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode)" : String,
  "[Ec2InstanceTypes](#cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes)" : [ String, ... ],
  "[MaxSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes)" : Double,
  "[MaxStoppedSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxstoppedsessionlengthinminutes)" : Double,
  "[SessionStorage](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionstorage)" : StreamConfigurationSessionStorage,
  "[StreamingImageIds](#cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax.yaml"></a>

```
  [ClipboardMode](#cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode): String
  [Ec2InstanceTypes](#cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes): 
    - String
  [MaxSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes): Double
  [MaxStoppedSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxstoppedsessionlengthinminutes): Double
  [SessionStorage](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionstorage): 
    StreamConfigurationSessionStorage
  [StreamingImageIds](#cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids): 
    - String
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-properties"></a>

`ClipboardMode`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode"></a>
Enable or disable the use of the system clipboard to copy and paste between the streaming session and streaming client\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceTypes`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes"></a>
The EC2 instance types that users can select from when launching a streaming session with this launch profile\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSessionLengthInMinutes`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes"></a>
The length of time, in minutes, that a streaming session can be active before it is stopped or terminated\. After this point, Nimble Studio automatically terminates or stops the session\. The default length of time is 690 minutes, and the maximum length of time is 30 days\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxStoppedSessionLengthInMinutes`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-maxstoppedsessionlengthinminutes"></a>
Integer that determines if you can start and stop your sessions and how long a session can stay in the STOPPED state\. The default value is 0\. The maximum value is 5760\.  
If the value is missing or set to 0, your sessions can’t be stopped\. If you then call `StopStreamingSession`, the session fails\. If the time that a session stays in the READY state exceeds the `maxSessionLengthInMinutes` value, the session will automatically be terminated \(instead of stopped\)\.  
If the value is set to a positive number, the session can be stopped\. You can call `StopStreamingSession` to stop sessions in the READY state\. If the time that a session stays in the READY state exceeds the `maxSessionLengthInMinutes` value, the session will automatically be stopped \(instead of terminated\)\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionStorage`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-sessionstorage"></a>
\(Optional\) The upload storage for a streaming session\.  
*Required*: No  
*Type*: [StreamConfigurationSessionStorage](aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamingImageIds`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids"></a>
The streaming images that users can select from when launching a streaming session with this launch profile\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
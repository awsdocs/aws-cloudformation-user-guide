# AWS::NimbleStudio::LaunchProfile StreamConfiguration<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration"></a>

A configuration for a streaming session\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax.json"></a>

```
{
  "[AutomaticTerminationMode](#cfn-nimblestudio-launchprofile-streamconfiguration-automaticterminationmode)" : String,
  "[ClipboardMode](#cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode)" : String,
  "[Ec2InstanceTypes](#cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes)" : [ String, ... ],
  "[MaxSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes)" : Double,
  "[MaxStoppedSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxstoppedsessionlengthinminutes)" : Double,
  "[SessionBackup](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionbackup)" : StreamConfigurationSessionBackup,
  "[SessionPersistenceMode](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionpersistencemode)" : String,
  "[SessionStorage](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionstorage)" : StreamConfigurationSessionStorage,
  "[StreamingImageIds](#cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids)" : [ String, ... ],
  "[VolumeConfiguration](#cfn-nimblestudio-launchprofile-streamconfiguration-volumeconfiguration)" : VolumeConfiguration
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax.yaml"></a>

```
  [AutomaticTerminationMode](#cfn-nimblestudio-launchprofile-streamconfiguration-automaticterminationmode): String
  [ClipboardMode](#cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode): String
  [Ec2InstanceTypes](#cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes): 
    - String
  [MaxSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes): Double
  [MaxStoppedSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxstoppedsessionlengthinminutes): Double
  [SessionBackup](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionbackup): 
    StreamConfigurationSessionBackup
  [SessionPersistenceMode](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionpersistencemode): String
  [SessionStorage](#cfn-nimblestudio-launchprofile-streamconfiguration-sessionstorage): 
    StreamConfigurationSessionStorage
  [StreamingImageIds](#cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids): 
    - String
  [VolumeConfiguration](#cfn-nimblestudio-launchprofile-streamconfiguration-volumeconfiguration): 
    VolumeConfiguration
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-properties"></a>

`AutomaticTerminationMode`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-automaticterminationmode"></a>
Indicates if a streaming session created from this launch profile should be terminated automatically or retained without termination after being in a `STOPPED` state\.  
+ When `ACTIVATED`, the streaming session is scheduled for termination after being in the `STOPPED` state for the time specified in `maxStoppedSessionLengthInMinutes`\.
+ When `DEACTIVATED`, the streaming session can remain in the `STOPPED` state indefinitely\.
This parameter is only allowed when `sessionPersistenceMode` is `ACTIVATED`\. When allowed, the default value for this parameter is `DEACTIVATED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClipboardMode`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode"></a>
Allows or deactivates the use of the system clipboard to copy and paste between the streaming session and streaming client\.  
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
Integer that determines if you can start and stop your sessions and how long a session can stay in the `STOPPED` state\. The default value is 0\. The maximum value is 5760\.  
This field is allowed only when `sessionPersistenceMode` is `ACTIVATED` and `automaticTerminationMode` is `ACTIVATED`\.  
If the value is set to 0, your sessions can’t be `STOPPED`\. If you then call `StopStreamingSession`, the session fails\. If the time that a session stays in the `READY` state exceeds the `maxSessionLengthInMinutes` value, the session will automatically be terminated \(instead of `STOPPED`\)\.  
If the value is set to a positive number, the session can be stopped\. You can call `StopStreamingSession` to stop sessions in the `READY` state\. If the time that a session stays in the `READY` state exceeds the `maxSessionLengthInMinutes` value, the session will automatically be stopped \(instead of terminated\)\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionBackup`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-sessionbackup"></a>
Information about the streaming session backup\.  
*Required*: No  
*Type*: [StreamConfigurationSessionBackup](aws-properties-nimblestudio-launchprofile-streamconfigurationsessionbackup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionPersistenceMode`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-sessionpersistencemode"></a>
Determine if a streaming session created from this launch profile can configure persistent storage\. This means that `volumeConfiguration` and `automaticTerminationMode` are configured\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionStorage`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-sessionstorage"></a>
The upload storage for a streaming session\.  
*Required*: No  
*Type*: [StreamConfigurationSessionStorage](aws-properties-nimblestudio-launchprofile-streamconfigurationsessionstorage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamingImageIds`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids"></a>
The streaming images that users can select from when launching a streaming session with this launch profile\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeConfiguration`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-volumeconfiguration"></a>
Custom volume configuration for the root volumes that are attached to streaming sessions\.  
This parameter is only allowed when `sessionPersistenceMode` is `ACTIVATED`\.  
*Required*: No  
*Type*: [VolumeConfiguration](aws-properties-nimblestudio-launchprofile-volumeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
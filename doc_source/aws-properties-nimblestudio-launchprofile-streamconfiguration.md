# AWS::NimbleStudio::LaunchProfile StreamConfiguration<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration"></a>

A configuration for a streaming session\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax.json"></a>

```
{
  "[ClipboardMode](#cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode)" : String,
  "[Ec2InstanceTypes](#cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes)" : StreamingInstanceTypeList,
  "[MaxSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes)" : Double,
  "[StreamingImageIds](#cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids)" : StreamingImageIdList
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streamconfiguration-syntax.yaml"></a>

```
  [ClipboardMode](#cfn-nimblestudio-launchprofile-streamconfiguration-clipboardmode): String
  [Ec2InstanceTypes](#cfn-nimblestudio-launchprofile-streamconfiguration-ec2instancetypes): 
    StreamingInstanceTypeList
  [MaxSessionLengthInMinutes](#cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes): Double
  [StreamingImageIds](#cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids): 
    StreamingImageIdList
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
*Type*: [StreamingInstanceTypeList](aws-properties-nimblestudio-launchprofile-streaminginstancetypelist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSessionLengthInMinutes`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-maxsessionlengthinminutes"></a>
The length of time, in minutes, that a streaming session can run\. After this point, Nimble Studio automatically terminates the session\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamingImageIds`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration-streamingimageids"></a>
The streaming images that users can select from when launching a streaming session with this launch profile\.  
*Required*: Yes  
*Type*: [StreamingImageIdList](aws-properties-nimblestudio-launchprofile-streamingimageidlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
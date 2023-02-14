# AWS::CodeGuruProfiler::ProfilingGroup Channel<a name="aws-properties-codeguruprofiler-profilinggroup-channel"></a>

Notification medium for users to get alerted for events that occur in application profile\. We support SNS topic as a notification channel\.

## Syntax<a name="aws-properties-codeguruprofiler-profilinggroup-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codeguruprofiler-profilinggroup-channel-syntax.json"></a>

```
{
  "[channelId](#cfn-codeguruprofiler-profilinggroup-channel-channelid)" : String,
  "[channelUri](#cfn-codeguruprofiler-profilinggroup-channel-channeluri)" : String
}
```

### YAML<a name="aws-properties-codeguruprofiler-profilinggroup-channel-syntax.yaml"></a>

```
  [channelId](#cfn-codeguruprofiler-profilinggroup-channel-channelid): String
  [channelUri](#cfn-codeguruprofiler-profilinggroup-channel-channeluri): String
```

## Properties<a name="aws-properties-codeguruprofiler-profilinggroup-channel-properties"></a>

`channelId`  <a name="cfn-codeguruprofiler-profilinggroup-channel-channelid"></a>
The channel ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`channelUri`  <a name="cfn-codeguruprofiler-profilinggroup-channel-channeluri"></a>
The channel URI\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
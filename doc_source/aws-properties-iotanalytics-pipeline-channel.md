# AWS IoT Analytics Pipeline Channel<a name="aws-properties-iotanalytics-pipeline-channel"></a>

<a name="aws-properties-iotanalytics-pipeline-channel-description"></a>The `Channel` property type specifies the source of messages to be processed for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-channel-inheritance"></a> `Channel` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-channel-syntax.json"></a>

```
{
  "[ChannelName](#cfn-iotanalytics-pipeline-channel-channelname)" : String,
  "[Name](#cfn-iotanalytics-pipeline-channel-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-channel-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-channel-syntax.yaml"></a>

```
[ChannelName](#cfn-iotanalytics-pipeline-channel-channelname): String
[Name](#cfn-iotanalytics-pipeline-channel-name): String
[Next](#cfn-iotanalytics-pipeline-channel-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-channel-properties"></a>

`ChannelName`  <a name="cfn-iotanalytics-pipeline-channel-channelname"></a>
The name of the channel from which the messages are processed\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-channel-name"></a>
The name of the 'channel' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-channel-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-channel-seealso"></a>
+ [ CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *AWS IoT Analytics User Guide*
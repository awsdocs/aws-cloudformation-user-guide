# AWS::MediaLive::Channel OutputDestination<a name="aws-properties-medialive-channel-outputdestination"></a>

<a name="aws-properties-medialive-channel-outputdestination-description"></a>The `OutputDestination` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::MediaLive::Channel](aws-resource-medialive-channel.md)\.

## Syntax<a name="aws-properties-medialive-channel-outputdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-outputdestination-syntax.json"></a>

```
{
  "[Id](#cfn-medialive-channel-outputdestination-id)" : String,
  "[MediaPackageSettings](#cfn-medialive-channel-outputdestination-mediapackagesettings)" : [ MediaPackageOutputDestinationSettings, ... ],
  "[MultiplexSettings](#cfn-medialive-channel-outputdestination-multiplexsettings)" : MultiplexProgramChannelDestinationSettings,
  "[Settings](#cfn-medialive-channel-outputdestination-settings)" : [ OutputDestinationSettings, ... ]
}
```

### YAML<a name="aws-properties-medialive-channel-outputdestination-syntax.yaml"></a>

```
  [Id](#cfn-medialive-channel-outputdestination-id): String
  [MediaPackageSettings](#cfn-medialive-channel-outputdestination-mediapackagesettings): 
    - MediaPackageOutputDestinationSettings
  [MultiplexSettings](#cfn-medialive-channel-outputdestination-multiplexsettings): 
    MultiplexProgramChannelDestinationSettings
  [Settings](#cfn-medialive-channel-outputdestination-settings): 
    - OutputDestinationSettings
```

## Properties<a name="aws-properties-medialive-channel-outputdestination-properties"></a>

`Id`  <a name="cfn-medialive-channel-outputdestination-id"></a>
User\-specified id\. This is used in an output group or an output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaPackageSettings`  <a name="cfn-medialive-channel-outputdestination-mediapackagesettings"></a>
Destination settings for a MediaPackage output; one destination for both encoders\.  
*Required*: No  
*Type*: List of [MediaPackageOutputDestinationSettings](aws-properties-medialive-channel-mediapackageoutputdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiplexSettings`  <a name="cfn-medialive-channel-outputdestination-multiplexsettings"></a>
Destination settings for a Multiplex output; one destination for both encoders\.  
*Required*: No  
*Type*: [MultiplexProgramChannelDestinationSettings](aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Settings`  <a name="cfn-medialive-channel-outputdestination-settings"></a>
Destination settings for a standard output; one destination for each redundant encoder\.  
*Required*: No  
*Type*: List of [OutputDestinationSettings](aws-properties-medialive-channel-outputdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
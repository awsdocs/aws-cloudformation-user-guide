# AWS::MediaLive::Channel OutputDestination<a name="aws-properties-medialive-channel-outputdestination"></a>

Contains information about the destinations for one output group in the channel\. In this element, include only one of the "settings" child elements, depending on the type of the output group that this destination information belongs to\. This element is part of an array at the top\-level of the channel\. 

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
An ID for this destination information\. Must be unique in the channel\. This ID associates this destination information with its output group\.  
For most output groups, enter a value there, then enter the same value in the destinaton field in the output group\.  
For an RTMP output group or Multiplex output group, enter a value here, then enter the same value in the destination field in the output \(not the output group\)\.  
For a MediaPackage output group, this ID is not used to make this association\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaPackageSettings`  <a name="cfn-medialive-channel-outputdestination-mediapackagesettings"></a>
Include this element if this destination information is for a MediaPackage output group\. Always create an array of one MediaPackageOutputDestinationSettings\.  
*Required*: No  
*Type*: List of [MediaPackageOutputDestinationSettings](aws-properties-medialive-channel-mediapackageoutputdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiplexSettings`  <a name="cfn-medialive-channel-outputdestination-multiplexsettings"></a>
Include this element if this destination information is for a Multiplex output group\. Create an array of one Create an array of two MultiplexProgramChannelDestinationSettings, because Multiplex output groups always require a standard channel\.  
*Required*: No  
*Type*: [MultiplexProgramChannelDestinationSettings](aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Settings`  <a name="cfn-medialive-channel-outputdestination-settings"></a>
Include this element if this destination information is for any output group except MediaPackage or Multiplex\. Create an array of one OutputDestinationSettings if the output group is in a single\-pipeline channel\. Create an array of two OutputDestinationSettings if it's in a standard channel\.  
*Required*: No  
*Type*: List of [OutputDestinationSettings](aws-properties-medialive-channel-outputdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
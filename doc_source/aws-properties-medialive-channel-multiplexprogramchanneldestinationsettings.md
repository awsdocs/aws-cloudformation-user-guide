# AWS::MediaLive::Channel MultiplexProgramChannelDestinationSettings<a name="aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings"></a>

Multiplex Program Input Destination Settings for outputting a Channel to a Multiplex

## Syntax<a name="aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings-syntax.json"></a>

```
{
  "[MultiplexId](#cfn-medialive-channel-multiplexprogramchanneldestinationsettings-multiplexid)" : String,
  "[ProgramName](#cfn-medialive-channel-multiplexprogramchanneldestinationsettings-programname)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings-syntax.yaml"></a>

```
  [MultiplexId](#cfn-medialive-channel-multiplexprogramchanneldestinationsettings-multiplexid): String
  [ProgramName](#cfn-medialive-channel-multiplexprogramchanneldestinationsettings-programname): String
```

## Properties<a name="aws-properties-medialive-channel-multiplexprogramchanneldestinationsettings-properties"></a>

`MultiplexId`  <a name="cfn-medialive-channel-multiplexprogramchanneldestinationsettings-multiplexid"></a>
The ID of the Multiplex that the encoder is providing output to\. You do not need to specify the individual inputs to the Multiplex; MediaLive will handle the connection of the two MediaLive pipelines to the two Multiplex instances\. The Multiplex must be in the same region as the Channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramName`  <a name="cfn-medialive-channel-multiplexprogramchanneldestinationsettings-programname"></a>
The program name of the Multiplex program that the encoder is providing output to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::MediaLive::Channel MultiplexOutputSettings<a name="aws-properties-medialive-channel-multiplexoutputsettings"></a>

Multiplex Output Settings

## Syntax<a name="aws-properties-medialive-channel-multiplexoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-multiplexoutputsettings-syntax.json"></a>

```
{
  "[Destination](#cfn-medialive-channel-multiplexoutputsettings-destination)" : OutputLocationRef
}
```

### YAML<a name="aws-properties-medialive-channel-multiplexoutputsettings-syntax.yaml"></a>

```
  [Destination](#cfn-medialive-channel-multiplexoutputsettings-destination): 
    OutputLocationRef
```

## Properties<a name="aws-properties-medialive-channel-multiplexoutputsettings-properties"></a>

`Destination`  <a name="cfn-medialive-channel-multiplexoutputsettings-destination"></a>
Destination is a Multiplex\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
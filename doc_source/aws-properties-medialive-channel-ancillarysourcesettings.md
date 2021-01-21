# AWS::MediaLive::Channel AncillarySourceSettings<a name="aws-properties-medialive-channel-ancillarysourcesettings"></a>

Ancillary Source Settings

## Syntax<a name="aws-properties-medialive-channel-ancillarysourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-ancillarysourcesettings-syntax.json"></a>

```
{
  "[SourceAncillaryChannelNumber](#cfn-medialive-channel-ancillarysourcesettings-sourceancillarychannelnumber)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-ancillarysourcesettings-syntax.yaml"></a>

```
  [SourceAncillaryChannelNumber](#cfn-medialive-channel-ancillarysourcesettings-sourceancillarychannelnumber): Integer
```

## Properties<a name="aws-properties-medialive-channel-ancillarysourcesettings-properties"></a>

`SourceAncillaryChannelNumber`  <a name="cfn-medialive-channel-ancillarysourcesettings-sourceancillarychannelnumber"></a>
Specifies the number \(1 to 4\) of the captions channel you want to extract from the ancillary captions\. If you plan to convert the ancillary captions to another format, complete this field\. If you plan to choose Embedded as the captions destination in the output \(to pass through all the channels in the ancillary captions\), leave this field blank because MediaLive ignores the field\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
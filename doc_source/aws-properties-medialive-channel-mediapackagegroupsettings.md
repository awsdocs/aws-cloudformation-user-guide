# AWS::MediaLive::Channel MediaPackageGroupSettings<a name="aws-properties-medialive-channel-mediapackagegroupsettings"></a>

Identifies this output group as a MediaPackage output group, and configures all the parts of the output group except for its outputs\. This element belongs to OutputGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-mediapackagegroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mediapackagegroupsettings-syntax.json"></a>

```
{
  "[Destination](#cfn-medialive-channel-mediapackagegroupsettings-destination)" : OutputLocationRef
}
```

### YAML<a name="aws-properties-medialive-channel-mediapackagegroupsettings-syntax.yaml"></a>

```
  [Destination](#cfn-medialive-channel-mediapackagegroupsettings-destination): 
    OutputLocationRef
```

## Properties<a name="aws-properties-medialive-channel-mediapackagegroupsettings-properties"></a>

`Destination`  <a name="cfn-medialive-channel-mediapackagegroupsettings-destination"></a>
MediaPackage channel destination\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)